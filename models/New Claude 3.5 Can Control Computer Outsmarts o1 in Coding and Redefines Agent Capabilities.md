Header image:

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/202410240107689.png)

Tags: AI, LLM, Claude, Sonnet, Agent, Cursor

# New Claude 3.5 Can Control Computer: Outsmarts o1 in Coding and Redefines Agent Capabilities

## Anthropic’s Groundbreaking AI, Claude 3.5, Uses Computers Like a Human and Becomes a Game-Changer in Automation

## Authors

- [Zijian Yang](https://www.linkedin.com/in/zijian-yang/) (**ORCID:** [0009-0006-8301-7634](https://orcid.org/0009-0006-8301-7634))

## Introduction

Claude 3.5 Receives a Major Upgrade Overnight!

As anticipated, Anthropic AI made a significant move this week with the launch of Claude 3.5 Haiku. The newly upgraded Claude 3.5 Sonnet has also been released.

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/202410240107240.png)

[https://x.com/AnthropicAI/status/1848742740420341988](https://x.com/AnthropicAI/status/1848742740420341988)

However, the much-anticipated "Ultra" version, Opus, has yet to make an appearance.

Remarkably, the evolved Claude 3.5 Sonnet has surpassed OpenAI o1, establishing itself as the most powerful reasoning model. The new Claude 3.5 Sonnet scored 49% on the most challenging coding benchmark based on real GitHub issues, verified by SWE-Bench.

- Cosine Genie scored 43.8%
- o1-preview scored 41.4%
- o1-mini scored 35.8%

Claude is the undisputed leader among all models when it comes to writing code.

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/202410240107920.png)

[https://x.com/AnthropicAI/status/1848742740420341988](https://x.com/AnthropicAI/status/1848742740420341988)

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/202410240108011.png)

Claude 3.5 Haiku matches the performance of the previous top-tier Claude 3 Opus, while maintaining similar cost and speed to the previous generation Haiku.

Amazingly, Claude can now interact with a computer like a human, including viewing the screen, moving the cursor, clicking buttons, and typing text!

According to Anthropic's Head of Developer Relations, "computer usage" is the first step towards a new paradigm of human-computer interaction. It is also a fundamental capability that AI models should possess.

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/202410240108566.png)

[https://x.com/alexalbert__/status/1848758641353986365](https://x.com/alexalbert__/status/1848758641353986365)

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/202410240108162.png)

[https://x.com/alexalbert__/status/1848743056654405799](https://x.com/alexalbert__/status/1848743056654405799)

Many startups developing browser agents have suddenly become obsolete overnight.

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/202410240108906.png)

Netizens are exclaiming that agents and workflows are about to change dramatically...

## **AI That Can Use a Computer?**

During its public trial, Anthropic introduced a groundbreaking new feature: computer usage capability. Starting today, developers can guide Claude to use a computer like a human through an API.

Claude 3.5 Sonnet is the first model to offer this feature in the public trial.

Of course, this feature is still experimental, and its use can be somewhat clumsy and prone to errors. Anthropic has opted for an early release to gather developer feedback and improve it quickly.

Why train AI to operate a computer?

Anthropic states that over the past few years, powerful AI development has reached many milestones, such as executing complex logical reasoning and recognizing and understanding images.

The next breakthrough is AI operating computers! If models can use all software as directed without needing specially customized tools, this certainly represents the future direction.

### **Basic Computer Operations**

In this demo, an Anthropic researcher posed a highly challenging task to Claude:

> My friend is coming to San Francisco, and I want to watch the sunrise over the Golden Gate Bridge with him tomorrow morning. We're starting from Pacific Heights. Can you help us find an excellent viewing spot, check the driving time and sunrise time, and then schedule a calendar event so we have enough time to get there?
> 

Claude independently opened Google and began the search.

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/202410240108524.gif)

How far is the Golden Gate Bridge from the user's location? Claude can independently open a map to find the distance.

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/202410240108809.gif)

After gathering the necessary information, it opened the calendar and scheduled the event for its user.

For more demonstrations, check out the video:

[https://www.youtube.com/watch?v=jqx18KgIzAE](https://www.youtube.com/watch?v=jqx18KgIzAE)

### **Automated Website Coding**

The developer demonstrated how Claude controlled their laptop to smoothly complete a website programming task. First, Claude navigated to [Claude.ai](http://claude.ai/) in the developer's Chrome browser and instructed Claude to create a 90s-themed personal homepage.

It entered the URL, typed prompts, and sent a request to another Claude.

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/202410240109285.gif)

Claude.ai returned some code, and the rendered page looked impressive, but the developer wanted to make some modifications locally on their computer.

So, they instructed Claude to download the files and open them in VS Code. Claude successfully completed these tasks.

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/202410240109241.gif)

Then, the developer asked Claude to start a server to view the file in the browser.

Claude opened the VS Code terminal and attempted to start a server, but encountered an error: Python wasn't installed on the machine.

By reviewing the terminal output, Claude identified the issue itself and successfully ran the server using Python 3.

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/202410240109898.gif)

However, there was an error in the terminal output, and a file icon was missing at the top. The developer asked Claude to identify the error and fix it in the file.

Surprisingly, Claude found the line causing the error in VS Code, deleted the entire line, saved the file, and relaunched the website.

This time, the website displayed perfectly!

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/202410240110146.png)

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/202410240110566.png)

Full video：

[https://www.youtube.com/watch?v=vH2f7cjXjKI](https://www.youtube.com/watch?v=vH2f7cjXjKI)

### **Automated Data Retrieval for Form Filling**

Suppose we need to fill out a supplier request form from "Ant Equipment Company," but the necessary data is scattered across the computer. Can Claude help us with this?

It started by taking screenshots of the developer's screen and quickly noticed that Ant Equipment Company wasn't listed in the form.

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/202410240110707.gif)

At this point, it immediately switched to the CRM system to search for the company. After locating it, Claude scrolled through the page to find all the necessary information for the form and then submitted it.

This means many tedious tasks in our work can be delegated to Claude!

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/202410240110897.gif)

Now, this feature is available in the API.

Several well-known companies, such as Asana, Canva, Cognition, DoorDash, Replit, and The Browser Company, are exploring Claude's potential to execute complex tasks with multiple steps. For example, Replit is using Claude 3.5 Sonnet's computer usage and user interface navigation capabilities to develop features for the Replit Agent, allowing real-time evaluation during application development.

Full video:

[https://www.youtube.com/watch?v=ODaHJzOyVCQ](https://www.youtube.com/watch?v=ODaHJzOyVCQ)

### **Far Below Human Performance, but Promising Future**

How does the newly upgraded Claude 3.5 Sonnet perform in terms of computer usage?

In OSWorld testing, it scored 14.9% in tasks based solely on screenshots, significantly surpassing the second-ranked AI system, which scored 7.8%.

When allowed more operational steps to complete tasks, Claude's score increased to 22.0%.

This indicates that multiple interactions with the environment can optimize task performance.

While this result shows substantial improvement, it remains far below the human performance level of 72.36%.

This suggests that Claude 3.5 Sonnet still has significant room for improvement in the future.

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/202410240111466.png)

After all, some operations that humans perform effortlessly (scrolling, dragging, zooming) are currently quite challenging for Claude.

## **Upgraded Claude 3.5 Sonnet: The Coding King Surpasses o1**

In various industry benchmark tests, the upgraded Claude 3.5 Sonnet has shown comprehensive performance improvements.

Notably, it has achieved significant breakthroughs in tasks involving intelligent coding and tool usage.

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/202410240111176.png)

[https://assets.anthropic.com/m/1cd9d098ac3e6467/original/Claude-3-Model-Card-October-Addendum.pdf](https://assets.anthropic.com/m/1cd9d098ac3e6467/original/Claude-3-Model-Card-October-Addendum.pdf)

In terms of coding ability, its performance in the SWE-bench Verified test has significantly increased from 33.4% to 49.0%.

This surpasses all publicly available models, including inference models like OpenAI o1-preview and specialized systems designed for intelligent coding.

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/202410240111612.png)

[https://www.swebench.com/](https://www.swebench.com/)

Additionally, in the TAU-bench—a benchmark test evaluating the tool usage capabilities of intelligent agents—Claude 3.5 Sonnet also performed exceptionally well:

> Its score in the retail sector increased from 62.6% to 69.2%, and in the more challenging aviation sector, it rose from 36.0% to 46.0%.
> 

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/202410240111508.png)

From the table below, it is evident that the new Claude 3.5 Sonnet significantly outperforms GPT-4o on the GPQA (Diamond) inference test benchmark.

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/202410240111210.png)

In visual QA, mathematical reasoning, document visual question answering, chart question answering, and scientific table benchmarks, Claude 3.5 Sonnet has set a new industry standard for performance.

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/202410240111887.png)

Notably, while the upgraded Claude 3.5 Sonnet has achieved performance breakthroughs, it maintains the same price and speed as its predecessor.

Feedback from early test users further confirms that the upgraded Claude 3.5 Sonnet represents a significant leap in AI-driven coding.

1. **GitLab:** In DevSecOps task tests, they observed a significant improvement in inference capabilities (up to a 10% increase in various use cases) without added latency, making it an ideal choice for driving complex software development processes.
2. **Cognition:** When applying the new Claude 3.5 Sonnet for autonomous AI assessments, it showed substantial improvements in coding, planning, and problem-solving compared to the previous model.
3. **The Browser Company:** In automating web workflows, they found Claude 3.5 Sonnet outperformed all previously tested models.

Additionally, before secure deployment, Claude 3.5 Sonnet underwent joint testing at the US AI Safety Institute (US AISI) and the UK AI Safety Institute (UK AISI).

Moreover, Anthropic's "Responsible Scaling Policy" ASL-2 standard still applies to the new model after its evaluation.

As previously mentioned, the upgraded Claude 3.5 Sonnet is now available for use on web and terminal apps.

API pricing starts at **$3 per million input tokens** and **$15 per million output tokens**.

Utilizing intelligent caching technology can save up to 90% in costs, while using batch processing APIs can reduce costs by 50%.

### **Applications**

Claude 3.5 Sonnet can understand nuanced instructions and context, recognize and correct its own errors, and generate in-depth analysis and insights from complex data. Coupled with cutting-edge coding, visual recognition, and writing abilities, Claude 3.5 Sonnet can be applied to a variety of scenarios.

- **Simulating Human Computer Interaction**

Through API integration, developers can guide Claude to use computers like a human—by observing the screen, moving the mouse, clicking buttons, and typing text. Claude 3.5 Sonnet is the first advanced AI model capable of reliably using a computer in this manner. Although still experimental, its capabilities will continue to improve over time.

- **Automated Code Generation**

Claude 3.5 Sonnet can assist throughout the software development lifecycle—from initial design to bug fixes, system maintenance to performance optimization. It can be directly integrated into products or used as an intelligent coding assistant via the [Claude.ai](http://claude.ai/) platform.

- **Intelligent Conversational Systems**

With enhanced reasoning abilities and a friendly, natural tone, Claude 3.5 Sonnet is ideal for developing intelligent conversational systems that need to connect data across systems and perform actions.

- **Intelligent Knowledge Q&A**

Claude 3.5 Sonnet's large-scale context processing capabilities and extremely low hallucination rate make it an ideal choice for handling Q&A tasks involving large knowledge bases, documents, and code repositories.

- **Visual Information Extraction**

Claude 3.5 Sonnet can effortlessly extract information from visual materials such as charts, graphs, and complex schematics, making it an ideal AI model for data analysis and data science tasks.

- **Process Automation**

Claude 3.5 Sonnet can automate repetitive tasks or processes. Its industry-leading command execution capabilities enable it to handle complex processes and operations.

## **New Claude 3.5 Haiku: Intelligently Surpassing Its Predecessor**

Compared to the previous generation, Claude 3.5 Haiku is considered the "smallest cup."

It is Anthropic's fastest model.

Not only does it maintain the same operating cost and similar processing speed as Claude 3 Haiku, but it has also achieved comprehensive skill enhancements.

In fact, in several intelligence benchmarks, Claude 3.5 Haiku **outperformed the previous most powerful model, Claude 3 Opus**.

Similarly, Claude 3.5 Haiku excels in coding tasks.

For instance, it scored an impressive 40.6% in the SWE-bench Verified test, **surpassing** many AI agents using publicly available state-of-the-art models, including the original versions of **Claude 3.5 Sonnet and GPT-4o**.

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/202410240111929.png)

Claude 3.5 Haiku boasts three standout advantages:

**1. Low-latency response**

**2. More precise instruction execution**

**3. More accurate tool usage**

These features make the model particularly suitable for user-facing product development, handling specialized sub-agent tasks, and creating personalized experiences based on large datasets, such as purchase records, pricing information, or inventory data.

By the end of this month, Claude 3.5 Haiku will be launched on multiple platforms, including the Anthropic API, Amazon Bedrock, and Google Cloud's Vertex AI. Initially, it will be available as a text-only model, with image input capabilities to be added later.

Pricing for Claude 3.5 Haiku starts at **$0.25 per million input tokens** and **$1.25 per million output tokens**.

Using prompt caching technology can save up to 90% in costs, while utilizing message batching APIs can reduce costs by 50%.

### **Applications**

With its fast processing speed, improved instruction execution capabilities, and more accurate tool usage, Claude 3.5 Haiku is well-suited for user-facing products, specialized auxiliary tasks, and generating personalized experiences from large datasets.

- **Code Auto-Completion**

Claude 3.5 Haiku can provide quick, accurate code suggestions and completions, effectively accelerating development workflows. It is particularly beneficial for software development teams looking to streamline coding processes and boost productivity.

- **Intelligent Chatbots**

With enhanced conversational abilities and rapid response times, Claude 3.5 Haiku excels in powering responsive chatbots capable of handling high volumes of user interactions. It is especially valuable for customer service, e-commerce, and educational platforms that require scalable interaction capabilities.

- **Data Extraction and Auto-Labeling**

Claude 3.5 Haiku efficiently processes and categorizes information, excelling in rapid data extraction and auto-labeling tasks. This capability is particularly useful for organizations that need to handle large volumes of unstructured data in financial, healthcare, and research fields.

- **Automated Real-Time Content Moderation**

Through its improved reasoning and content understanding abilities, Claude 3.5 Haiku provides reliable, real-time content moderation services. This is invaluable for social platforms, online communities, and media organizations that need to maintain safe and appropriate content at scale.

## **Teaching Claude to Operate a Computer**

Anthropic notes that operations humans execute effortlessly—scrolling, dragging, zooming—remain challenging for Claude.

For risks like spam, misinformation, and fraud, the company is seeking safe deployment strategies, such as developing recognition systems to detect harmful activities.

### **Research Process**

Anthropic's work in tool usage and multimodal capabilities lays the groundwork for AI to recognize and interpret images.

Building on this, Claude must reason about how and when to perform actions based on screen content.

To this end, researchers trained Claude to accurately compute pixels to complete commands, as it must calculate the number of pixels to move the mouse pointer vertically or horizontally to click the correct spot.

During this process, Claude quickly transferred learning from simple software like calculators and text editors to other applications (note that it was not allowed internet access during this time).

This training allows it to translate user instructions into a series of logical steps to perform tasks. It can even self-correct and retry tasks when encountering obstacles.

### **A Little Anecdote**

Alex Albert, Anthropic’s Head of Developer Relations, shared a fun story from when the team was developing the computer usage feature.

They organized a bug bash with engineers to ensure all potential issues with the API were identified.

This meant locking a group of engineers in a room for several hours.

Coincidentally, everyone was hungry, and one engineer had a sudden idea: "Why not let Claude perform a live drill and autonomously open DoorDash to order us some food?"

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/202410240112840.png)

Surprisingly, about a minute later, Claude had ordered pizza for the engineers.

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/202410240112633.png)

### **Looking Ahead**

The ability for AI to operate a computer represents a new approach in artificial intelligence development.

Until now, LLM developers have worked to adapt tools to the model, creating specialized environments where AI uses purpose-built tools to accomplish various tasks.

Now, Anthropic is taking the opposite approach—letting the model adapt to the tools. This means that Claude can integrate into the computer environment we use daily, directly utilizing existing software like a human.

Although Claude has reached the current highest level, its operations are still relatively slow and prone to errors. Many actions we perform daily on computers, such as dragging and zooming, are still beyond Claude's capabilities.

Additionally, Claude observes the screen in a way similar to flipping through a "picture book" — taking a series of screenshots and stitching them together, rather than watching a continuous video stream. This means it might miss some fleeting actions or notifications.

Interestingly, Anthropic encountered some amusing incidents while recording demos.

For instance, during one demonstration, Claude accidentally clicked to stop a long-running screen recording, causing all the footage to be lost.

In another coding demonstration, Claude suddenly "zoned out" and started browsing photos of Yellowstone National Park with great interest.

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/202410240112480.gif)

In summary, Claude's current performance inspires great anticipation for the future: the ability of AI to operate computers will advance rapidly, making it easy for even novice software developers to utilize it.

## **Conclusion**

In conclusion, the recent advancements in Claude 3.5 Sonnet and Haiku mark a significant leap forward in AI capabilities, particularly in intelligent coding and human-computer interaction. With the ability to operate computers, generate complex code, and assist in various automation tasks, Claude is poised to revolutionize workflows across industries. While the technology is still in its early stages, the potential for further development and refinement promises exciting applications in the near future, reshaping how we interact with AI-driven systems in everyday tasks.

## **Source**

- [https://assets.anthropic.com/m/1cd9d098ac3e6467/original/Claude-3-Model-Card-October-Addendum.pdf](https://assets.anthropic.com/m/1cd9d098ac3e6467/original/Claude-3-Model-Card-October-Addendum.pdf)
- [https://www.anthropic.com/news/3-5-models-and-computer-use](https://www.anthropic.com/news/3-5-models-and-computer-use)