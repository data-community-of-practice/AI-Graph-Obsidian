![Logo](https://www.blackforestlabs.ai/wp-content/uploads/2024/07/logo-with-text_more-1024x970.png)
<div align="center" ><i>Source : blackforestlabs.ai</i></div>
# **Author**

Tarun Krishnan (**ORCID**: [0009-0006-6647-127X](https://orcid.org/0009-0006-6647-127X))

# **Introduction**

With the growing demand for **image generation models** in various applications, the need for **APIs** that seamlessly integrate these models into developers' workflows has skyrocketed. Rather than relying solely on company interfaces or restricted platforms, developers are looking for _flexible_ and _scalable_ solutions that allow them to embed cutting-edge generative models directly into their own applications. APIs have become the bridge that connects innovation with real-world usability.

One such advancement is **FLUX1.1 [pro]**, a state-of-the-art image generation model that stands out for its remarkable speed, high fidelity, and impressive diversity in outputs. **FLUX1.1 [pro]** has rapidly gained traction due to its performance, which is six times faster than its predecessor, _FLUX.1 [pro]_. This improvement in both speed and quality has made it an attractive option for creative professionals and enterprises alike.

To extend the capabilities of **FLUX1.1 [pro]** to a wider audience, **Black Forest Labs** has introduced the **BFL API**. This API allows developers and businesses to integrate FLUX’s powerful image generation models directly into their own systems, offering flexibility in _customization_, _scalability_, and _cost-effectiveness_. The **BFL API** opens doors for creators looking to build bespoke applications with cutting-edge generative AI, without the need for specialized hardware or deep technical expertise.

# **What is FLUX1.1 [pro]?**

Before delving into the **BFL API**, it's important to understand the power behind **FLUX1.1 [pro]**, the latest image generation model developed by Black Forest Labs. This model offers substantial improvements in speed and performance, providing up to six times faster generation than its predecessor, **FLUX.1 [pro]**. Such advancements allow developers and creators to work more efficiently, delivering high-quality images in significantly less time.

![bfl1](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/bfl-1.png)

<div align="center" ><i>FLUX1.1 [pro] Image Generation Examples, Source : blackforestlabs.ai</i></div>
### Why Choose FLUX1.1 [pro]?

- **Speed and Efficiency**: The model strikes an ideal balance between image quality and inference speed, producing images three times faster than **FLUX.1 [pro]**, making it perfect for workflows that demand both speed and precision.

- **Performance at the Top of Its Class**: FLUX1.1 [pro] has been tested under the codename "_blueberry_" in the **Artificial Analysis image arena**, where it outperformed other models and achieved the highest overall Elo score. This places it at the forefront of text-to-image generation in terms of both quality and prompt accuracy.

![bfl2](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/bfl-2.png)
<div align="center" ><i>FLUX1.1 [pro] Elo Score: Performance Leader in Image Generation,  Source : blackforestlabs.ai</i></div>

![bfl3](https://blackforestlabs.ai/wp-content/uploads/2024/10/elo_vs_price-3-1536x1152.png)
<div align="center" ><i>FLUX1.1 [pro]: Elo Score vs. Cost Comparison of Leading Image Models,  Source : blackforestlabs.ai</i></div>

![bfl4](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/bfl-4.png)
<div align="center" ><i>FLUX1.1 [pro]: Elo Score vs. Speed Comparison of Image Generation Models,  Source : blackforestlabs.ai</i></div>

- **Upcoming High-Resolution Support**: Soon, the model will offer high-resolution image generation of up to 2K, enabling creators to produce detailed, high-fidelity visuals without sacrificing speed or accuracy.

These standout features make **FLUX1.1 [pro]** an attractive option for anyone in need of high-performance image generation. By using the **BFL API**, businesses and developers can easily tap into the potential of this powerful model, integrating it directly into their own applications for a seamless experience.


# **How to Use the BFL API**

In this guide, we’ll walk you through the steps to use the **BFL API** for generating stunning images using advanced models like **FLUX1.1 [pro]**. Whether you're a developer or a creator, this API allows you to integrate high-performance image generation into your applications effortlessly.

### **Step 1: Create a Black Forest Labs Account**

To get started, you need to create an account and obtain an API key. Follow these steps:

1. **Register**: Visit [api.bfl.ml](https://api.bfl.ml) and sign up for an account. You’ll receive a confirmation email to verify before you can log in.

   ![BFL Registration](https://docs.bfl.ml/assets/register.png)
   <div align="center"><i>BFL Platform Registration, Source: docs.bfl.ml</i></div>

2. **Create an API Key**: After logging in, create your `BFL API KEY` by clicking the **Add Key** button.

   ![Add Key](https://docs.bfl.ml/assets/api_key_0.png)
   <div align="center"><i>Click on + Add Key, Source: docs.bfl.ml</i></div>

3. **Name Your Key**: Name your key, then proceed to generate it.

   ![Name Key](https://docs.bfl.ml/assets/api_key_1.png)
   <div align="center"><i>Name your API Key, Source: docs.bfl.ml</i></div>

4. **View Your API Key**: You can now view and copy your API key, which is required for authentication.

   ![View Key](https://docs.bfl.ml/assets/api_key_2.png)
   <div align="center"><i>Your API Key, Source: docs.bfl.ml</i></div>

---

### **Step 2: Managing Your Credits**

With your account and API key ready, you now need to add credits to use the **BFL API** services.

- **Pricing**: The cost of generating images with **FLUX1.1 [pro]** is **$0.04 per image**. Other model prices include:
  - **FLUX.1 [pro]**: $0.05 per image
  - **FLUX.1 [dev]**: $0.025 per image

To add credits:

1. **Log in** to [api.bfl.ml](https://api.bfl.ml/) and click the **Add** button to purchase credits.

   ![Add Credits](https://docs.bfl.ml/assets/add_credits.png)
   <div align="center"><i>Select the amount of credits and click Add, Source: docs.bfl.ml</i></div>

2. **Payment**: You’ll be redirected to the Stripe payment interface to complete your transaction.

   ![Stripe Payment](https://docs.bfl.ml/assets/stripe.png)
   <div align="center"><i>Stripe Payment Screen, Source: docs.bfl.ml</i></div>

---

### **Step 3: Creating an Image Using the API**

Now that your account is set up and credits are loaded, it’s time to generate an image!

The **BFL API** uses an asynchronous design: you submit a request, then query for the result when it’s ready. The following endpoints are supported:
- `/flux-pro-1.1`
- `/flux-pro`
- `/flux-dev`

Let’s look at examples of how to create a request.

---

### **Python Implementation**

Install the `requests` library (e.g., `pip install requests`) and use the following code to send an image generation request:

```python
import os
import requests

request = requests.post(
    'https://api.bfl.ml/v1/flux-pro-1.1',
    headers={
        'accept': 'application/json',
        'x-key': os.environ.get("BFL_API_KEY"),
        'Content-Type': 'application/json',
    },
    json={
        'prompt': 'A cat on its back legs running like a human is holding a big silver fish with its arms. The cat is running away from the shop owner and has a panicked look on his face. The scene is situated in a crowded market.',
        'width': 1024,
        'height': 768,
    },
).json()
print(request)
request_id = request["id"]
```

This code sends a **POST** request to the **BFL API**. It includes:
- Headers like the **API key** (retrieved from your environment variables) and content type.
- A **JSON body** with the image generation prompt (e.g., a cat running with a fish) and dimensions.
- Once the request is submitted, the `request_id` is returned, which will be used to check the image generation status.

---

### **Polling for the Result**

Once the request is sent, you can poll the API for the result:

```python
import time

while True:
    time.sleep(0.5)
    result = requests.get(
        'https://api.bfl.ml/v1/get_result',
        headers={
            'accept': 'application/json',
            'x-key': os.environ.get("BFL_API_KEY"),
        },
        params={
            'id': request_id,
        },
    ).json()
    if result["status"] == "Ready":
        print(f"Result: {result['result']['sample']}")
        break
    else:
        print(f"Status: {result['status']}")
```

This snippet continuously checks the status of the image generation by sending repeated **GET** requests to the `get_result` endpoint. The code waits half a second between checks and, once the image is ready, prints the result. If the task is still in progress, it prints the current status.

---

### **Bash Implementation**

If you prefer using **bash**, here’s how you can achieve the same result using `curl`:

```bash
request=$(curl -X 'POST' \
  'https://api.bfl.ml/v1/flux-pro-1.1' \
  -H 'accept: application/json' \
  -H "x-key: ${BFL_API_KEY}" \
  -H 'Content-Type: application/json' \
  -d '{
  "prompt": "A cat on its back legs running like a human is holding a big silver fish with its arms. The cat is running away from the shop owner and has a panicked look on his face. The scene is situated in a crowded market.",
  "width": 1024,
  "height": 768
}')
echo $request
request_id=$(jq -r .id <<< $request)
```

This script sends a **POST** request to the BFL API using `curl`. It includes headers for authentication and content type, along with the image prompt and dimensions in the request body. The response contains the `request_id`, which is then extracted using `jq`.

---

### **Polling for the Result (Bash)**

To retrieve the image using **bash**, you can continuously poll the result as follows:

```bash
while true
do
  sleep 0.5
  result=$(curl -s -X 'GET' \
    "https://api.bfl.ml/v1/get_result?id=${request_id}" \
    -H 'accept: application/json' \
    -H "x-key: ${BFL_API_KEY}")
  if [ "$( jq -r .status <<< $result )" == "Ready" ]
  then
    echo "Result: $(jq -r .result.sample <<< $result)"
    break
  else
    echo "Status: $(jq -r .status <<< $result)"
  fi
done
```

This **bash script** repeatedly checks the status of the image generation using the `get_result` endpoint. Once the status becomes `"Ready"`, the image result is printed.

---

### **API Limits**

Please note the **BFL API** has the following limits:
- **Active Tasks**: You are limited to 12 active tasks. Exceeding this will result in a `429` status code.
- **Credits**: If you run out of credits, the API will return a `402` status code. You can add more credits by logging into [api.bfl.ml](https://api.bfl.ml).

If you need higher usage volumes, contact us at **flux@blackforestlabs.ai**.

---

This concludes the guide to using the **BFL API**. With simple steps, you can generate images efficiently while leveraging cutting-edge generative models like **FLUX1.1 [pro]**. Happy creating!

# Conclusion

As we continue to push the boundaries of what technology can achieve, the **BFL API** stands as a testament to the transformative power of AI-driven creativity. It offers more than just a tool—it provides a gateway to streamline innovation, enabling developers and creators to harness the power of models like **FLUX1.1 [pro]** with unprecedented ease. Reflecting on its potential, the BFL API represents a critical shift in how we think about integrating cutting-edge generative models into our workflows. It allows us to blur the lines between art and automation, code and creativity.

The true beauty of such tools lies not just in their capabilities, but in the opportunities they open for experimentation and expression. With speed, precision, and scalability, the BFL API encourages creators to think beyond technical constraints, pushing the boundaries of their imaginations. As developers continue to explore and iterate, the API promises to be a key player in shaping the future of generative AI in real-world applications. This evolution isn't just about creating images—it's about redefining the process of creation itself.

The journey is just beginning, and it's exciting to imagine what comes next when creativity is only a few lines of code away.

