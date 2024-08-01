Header image:

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/202408020448161.png)

Tags: AI, LLM, OpenAI, Assistants, API, ChatGPT

# How to Use OpenAI Assistants API to Build Your Own Custom ChatGPT?

## A Step-by-Step Guide to Creating Versatile AI Assistants Using OpenAI's Assistants API

## Authors

- [Zijian Yang](https://www.linkedin.com/in/zijian-yang/) (**ORCID:** [0009-0006-8301-7634](https://orcid.org/0009-0006-8301-7634))

## Introduction

The Assistants API is a powerful new offering that enables developers to integrate AI assistants directly into their applications. These assistants are designed to handle a wide range of user queries by utilizing models, tools, and files. The API currently supports three main types of tools: Code Interpreter, File Search, and Function Calling.

To get started with the Assistants API, developers can explore its capabilities through the [Assistants playground](https://platform.openai.com/playground/assistants) or follow a [step-by-step guide](https://platform.openai.com/docs/assistants/overview) available in the Assistants API quickstart. This API is in beta, and OpenAI is actively working on expanding its features. Developers are encouraged to share their feedback in the Developer Forum.

### How Assistants Work

The Assistants API provides developers with the tools to create versatile AI assistants. These assistants can call OpenAI’s models with specific instructions, allowing them to customize the personality and capabilities of the AI. They can also access multiple tools simultaneously, including both OpenAI-hosted tools like the Code Interpreter and File Search, as well as custom tools via function calling.

A unique feature of the Assistants API is its support for persistent Threads, which streamline AI application development by maintaining message history. This feature helps manage conversations, truncating history when it exceeds the model’s context length, ensuring efficient and coherent interactions.

Moreover, Assistants can access and handle various file formats, whether for initial setup or during interactions within Threads. They can create files such as images and spreadsheets or reference files within their responses, enhancing the assistant's utility and integration.

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/202408020448659.png)

| Object | What it represents |
| --- | --- |
| Assistant | Purpose-built AI that uses OpenAI’s https://platform.openai.com/docs/models and calls https://platform.openai.com/docs/assistants/tools |
| Thread | A conversation session between an Assistant and a user. Threads store Messages and automatically handle truncation to fit content into a model’s context. |
| Message | A message created by an Assistant or a user. Messages can include text, images, and other files. Messages stored as a list on the Thread. |
| Run | An invocation of an Assistant on a Thread. The Assistant uses its configuration and the Thread’s Messages to perform tasks by calling models and tools. As part of a Run, the Assistant appends Messages to the Thread. |
| Run Step | A detailed list of steps the Assistant took as part of a Run. An Assistant can call tools or create Messages during its run. Examining Run Steps allows you to introspect how the Assistant is getting to its final results. |

### What is the difference between OpenAI Assistant API and Chat API?

The Assistants API is distinct from the broader OpenAI API, which offers a wider array of capabilities including language modeling, image generation, and speech-to-text conversion. While the OpenAI API caters to diverse use cases like chatbots, content creation, and translation, the Assistants API is specifically geared towards building AI assistants with integrated tool support. Essentially, the Assistants API extends the functionality of the OpenAI API by providing additional tools and features, making it ideal for developing sophisticated assistant applications.

### What You'll Learn in This Article

In this article, you'll learn how to use OpenAI's Assistants API to build powerful GPT assistants. We will explore the core features of the Assistants API, including how to create and configure assistants, manage conversation threads, utilize tools like the Code Interpreter and File Search, and perform function calls. Through detailed examples and code snippets, this article will guide you step-by-step in implementing a versatile AI assistant capable of handling complex user queries and tasks. Whether you're a developer, a beginner, or simply interested in AI technology, this article will provide you with valuable knowledge and practical skills.

## **Assistants API Quickstart**

A typical integration of the Assistants API has the following flow:

1. Create an Assistant by defining its custom instructions and picking a model. If helpful, add files and enable tools like Code Interpreter, File Search, and Function calling.
2. Create a Thread when a user starts a conversation.
3. Add Messages to the Thread as the user asks questions.
4. Run the Assistant on the Thread to generate a response by calling the model and the tools.

This starter guide walks through the key steps to create and run an Assistant that uses Code Interpreter. In this example, we're creating an Assistant that is a personal math tutor, with the Code Interpreter tool enabled.

Calls to the Assistants API require that you pass a beta HTTP header. This is handled automatically if you’re using OpenAI’s official Python or Node.js SDKs. **`OpenAI-Beta: assistants=v2`**

**Step 1: Create an Assistant**

An Assistant represents an entity that can be configured to respond to a user's messages using several parameters like **`model`**, **`instructions`**, and **`tools`**.

```python
from openai import OpenAI
client = OpenAI()
  
assistant = client.beta.assistants.create(
  name="Math Tutor",
  instructions="You are a personal math tutor. Write and run code to answer math questions.",
  tools=[{"type": "code_interpreter"}],
  model="gpt-4o",
)
```

**Step 2: Create a Thread**

A Thread represents a conversation between a user and one or many Assistants. You can create a Thread when a user (or your AI application) starts a conversation with your Assistant.

```python
thread = client.beta.threads.create()
```

**Step 3: Add a Message to the Thread**

The contents of the messages your users or applications create are added as [Message](https://platform.openai.com/docs/api-reference/messages/object) objects to the Thread. Messages can contain both text and files. There is no limit to the number of Messages you can add to Threads — we smartly truncate any context that does not fit into the model's context window.

```python
message = client.beta.threads.messages.create(
  thread_id=thread.id,
  role="user",
  content="I need to solve the equation `3x + 11 = 14`. Can you help me?"
)
```

**Step 4: Create a Run**

Once all the user Messages have been added to the Thread, you can [Run](https://platform.openai.com/docs/api-reference/runs/object) the Thread with any Assistant. Creating a Run uses the model and tools associated with the Assistant to generate a response. These responses are added to the Thread as **`assistant`** Messages.

**With streaming**

You can use the 'create and stream' helpers in the Python and Node SDKs to create a run and stream the response.

```python
from typing_extensions import override
from openai import AssistantEventHandler
 
# First, we create a EventHandler class to define
# how we want to handle the events in the response stream.
 
class EventHandler(AssistantEventHandler):    
  @override
  def on_text_created(self, text) -> None:
    print(f"\nassistant > ", end="", flush=True)
      
  @override
  def on_text_delta(self, delta, snapshot):
    print(delta.value, end="", flush=True)
      
  def on_tool_call_created(self, tool_call):
    print(f"\nassistant > {tool_call.type}\n", flush=True)
  
  def on_tool_call_delta(self, delta, snapshot):
    if delta.type == 'code_interpreter':
      if delta.code_interpreter.input:
        print(delta.code_interpreter.input, end="", flush=True)
      if delta.code_interpreter.outputs:
        print(f"\n\noutput >", flush=True)
        for output in delta.code_interpreter.outputs:
          if output.type == "logs":
            print(f"\n{output.logs}", flush=True)
 
# Then, we use the `stream` SDK helper 
# with the `EventHandler` class to create the Run 
# and stream the response.
 
with client.beta.threads.runs.stream(
  thread_id=thread.id,
  assistant_id=assistant.id,
  instructions="Please address the user as Jane Doe. The user has a premium account.",
  event_handler=EventHandler(),
) as stream:
  stream.until_done()
```

**Without streaming**

Runs are asynchronous, which means you'll want to monitor their **`status`** by polling the Run object until a terminal status is reached. For convenience, the 'create and poll' SDK helpers assist both in creating the run and then polling for its completion.

```python
run = client.beta.threads.runs.create_and_poll(
  thread_id=thread.id,
  assistant_id=assistant.id,
  instructions="Please address the user as Jane Doe. The user has a premium account."
)
```

Once the Run completes, you can list the Messages added to the Thread by the Assistant.

```python
if run.status == 'completed': 
  messages = client.beta.threads.messages.list(
    thread_id=thread.id
  )
  print(messages)
else:
  print(run.status)
```

## Developing a Python Code Assistant

Based on what we've learned so far, let's put it into practice.

```python
import openai  # Import the OpenAI library

# Retrieve the API key from the environment variable OPENAI_API_KEY
OPENAI_API_KEY = ""
client = openai.OpenAI(api_key=OPENAI_API_KEY)

# Create an assistant named "Python Master" that generates runnable Python code based on the given instructions
assistant_python = client.beta.assistants.create(
    name="Python Master",
    instructions="You are a Python Expert. Generate runnable Python code according to messages.",
    tools=[{"type": "code_interpreter"}],  # Use the code interpreter tool
    model="gpt-4o",  # Use the GPT-4o model
)

# Create a communication thread
thread_python = client.beta.threads.create()

# Create a message in the thread
message = client.beta.threads.messages.create(
    thread_id=thread_python.id,
    role="user",
    content="How to write a quicksort algorithm?",
)

# Create and wait for the run to complete, handling the interaction and problem-solving in the thread
run = client.beta.threads.runs.create_and_poll(
    thread_id=thread_python.id,
    assistant_id=assistant_python.id,
)

print("Run completed with status: " + run.status)  # Print the run completion status

# If the run status is "completed", retrieve and print all messages
if run.status == "completed":
    messages = client.beta.threads.messages.list(thread_id=thread_python.id)

    print("\nMessages:\n")
    for message in messages:
        assert message.content[0].type == "text"
        print(f"Role: {message.role.capitalize()}")  # Capitalize the role name
        print("Message:")
        print(message.content[0].text.value + "\n")  # Add a newline after each message for readability
```

Output:

```python

Messages:

Role: Assistant
Message:
A Red-Black Tree is a self-balancing binary search tree where each node has an extra bit for denoting the color of the node, either red or black. The tree ensures that the paths from root to leaves have an approximately equal number of black nodes, ensuring the tree remains balanced and offers O(log n) time complexity for operations like insertion, deletion, and search.

Here are the key properties of a Red-Black Tree:
1. Each node is either red or black.
2. The root is black.
3. All leaves (NIL nodes) are black.
4. If a red node has children, then the children are always black (no two red nodes can be adjacent).
5. Every path from a node to its descendant NIL nodes has the same number of black nodes.

Creating a full Red-Black Tree implementation involves significant complexity, and typically specialized libraries (like `sortedcontainers` for Python, or using `TreeMap` in Java) handle these. However, I can show you a basic implementation of the insertion operation along with rebalancing.

```python
class Node:
    def __init__(self, data):
        self.data = data
        self.color = 'red'
        self.left = None
        self.right = None
        self.parent = None

class RedBlackTree:
    def __init__(self):
        self.NIL_LEAF = Node(None)
        self.NIL_LEAF.color = 'black'
        self.root = self.NIL_LEAF

    def insert(self, data):
        new_node = Node(data)
        new_node.left = self.NIL_LEAF
        new_node.right = self.NIL_LEAF

        if self.root == self.NIL_LEAF:
            new_node.color = 'black'
            self.root = new_node
        else:
            self._insert_helper(self.root, new_node)
            self.fix_insert(new_node)

    def _insert_helper(self, current, new_node):
        if new_node.data < current.data:
            if current.left == self.NIL_LEAF:
                current.left = new_node
                new_node.parent = current
            else:
                self._insert_helper(current.left, new_node)
        else:
            if current.right == self.NIL_LEAF:
                current.right = new_node
                new_node.parent = current
            else:
                self._insert_helper(current.right, new_node)

    def fix_insert(self, node):
        while node != self.root and node.parent.color == 'red':
            if node.parent == node.parent.parent.left:
                uncle = node.parent.parent.right
                if uncle.color == 'red':
                    node.parent.color = 'black'
                    uncle.color = 'black'
                    node.parent.parent.color = 'red'
                    node = node.parent.parent
                else:
                    if node == node.parent.right:
                        node = node.parent
                        self.left_rotate(node)
                    node.parent.color = 'black'
                    node.parent.parent.color = 'red'
                    self.right_rotate(node.parent.parent)
            else:
                uncle = node.parent.parent.left
                if uncle.color == 'red':
                    node.parent.color = 'black'
                    uncle.color = 'black'
                    node.parent.parent.color = 'red'
                    node = node.parent.parent
                else:
                    if node == node.parent.left:
                        node = node.parent
                        self.right_rotate(node)
                    node.parent.color = 'black'
                    node.parent.parent.color = 'red'
                    self.left_rotate(node.parent.parent)
        self.root.color = 'black'

    def left_rotate(self, node):
        right_child = node.right
        node.right = right_child.left
        if right_child.left != self.NIL_LEAF:
            right_child.left.parent = node
        right_child.parent = node.parent
        if node.parent is None:
            self.root = right_child
        elif node == node.parent.left:
            node.parent.left = right_child
        else:
            node.parent.right = right_child
        right_child.left = node
        node.parent = right_child

    def right_rotate(self, node):
        left_child = node.left
        node.left = left_child.right
        if left_child.right != self.NIL_LEAF:
            left_child.right.parent = node
        left_child.parent = node.parent
        if node.parent is None:
            self.root = left_child
        elif node == node.parent.right:
            node.parent.right = left_child
        else:
            node.parent.left = left_child
        left_child.right = node
        node.parent = left_child

    def inorder_traversal(self, node, result=None):
        if result is None:
            result = []
        if node != self.NIL_LEAF:
            self.inorder_traversal(node.left, result)
            result.append(node.data)
            self.inorder_traversal(node.right, result)
        return result

# Example Usage
rb_tree = RedBlackTree()
values = [20, 15, 25, 10, 5, 1, 30]

for value in values:
    rb_tree.insert(value)

sorted_values = rb_tree.inorder_traversal(rb_tree.root)
sorted_values  # This should return an in-order traversal of the tree, which is the sorted order of elements
```

This code defines a Red-Black Tree with insertion and basic rebalancing. The `fix_insert` function ensures that the tree maintains its properties after each insertion. The `inorder_traversal` function can be used to retrieve a sorted list of elements from the tree, demonstrating that the tree operations work as intended. 

Feel free to ask for any additional operations or if you have any questions!

Role: User
Message:
How about red black tree?

Role: Assistant
Message:
The quick sort algorithm has successfully sorted the array `[3, 6, 8, 10, 1, 2, 1]` into `[1, 1, 2, 3, 6, 8, 10]`.

This implementation of quick sort is easy to understand but can be optimized. For example, the current implementation makes additional list allocations. In practice, an in-place version of quick sort is often preferred for better space efficiency.

If you have any further questions or need additional modifications, feel free to ask!

Role: Assistant
Message:
Quick sort is a popular and efficient sorting algorithm that uses a divide-and-conquer strategy to sort an array. The algorithm works by selecting a "pivot" element from the array and partitioning the other elements into two sub-arrays: those less than the pivot and those greater than or equal to the pivot. The process is then recursively applied to the sub-arrays.

Here is a basic implementation of the quick sort algorithm in Python:

```python
def quick_sort(arr):
    if len(arr) <= 1:
        return arr
    else:
        pivot = arr[len(arr) // 2]
        left = [x for x in arr if x < pivot]
        middle = [x for x in arr if x == pivot]
        right = [x for x in arr if x > pivot]
        return quick_sort(left) + middle + quick_sort(right)

# Example usage:
arr = [3, 6, 8, 10, 1, 2, 1]
sorted_arr = quick_sort(arr)
print(sorted_arr)
```

In the code above:
1. We define the `quick_sort` function that takes an array `arr` as input.
2. If the length of the array is less than or equal to 1, it is already sorted, so we return it.
3. We select the pivot element as the middle element of the array.
4. We then create three sub-arrays: `left` containing elements less than the pivot, `middle` containing elements equal to the pivot, and `right` containing elements greater than the pivot.
5. We recursively apply `quick_sort` to the `left` and `right` sub-arrays and concatenate the results with the `middle` array to get the sorted array.

Let's run this code to see if it works properly:

Role: User
Message:
How to write a quick sort?

```

## **Conclusion**

In summary, the Assistants API offers a robust platform for developers to integrate advanced AI assistants into their applications. By leveraging tools like the Code Interpreter, File Search, and Function Calling, developers can create specialized assistants capable of handling a wide range of tasks. The API's support for persistent Threads ensures efficient management of user interactions, maintaining context and coherence in conversations. As OpenAI continues to expand the capabilities of the Assistants API, developers have an exciting opportunity to build more sophisticated and responsive AI-driven solutions, enhancing user experiences and streamlining workflows across various industries.

## **Source**

- [https://platform.openai.com/docs/assistants/quickstart?context=without-streaming](https://platform.openai.com/docs/assistants/quickstart?context=without-streaming)