Header image:

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/202412110029061.png)

Tags: AI, LLM, FLUX 1.1, FLUX.1

# How to Use FLUX 1.1 Online for Free: A Tutorial on Generating Ultra Realistic Images and Editing Tools

## A Step-by-Step Guide to Using FLUX 1.1, FLUX Fill, Canny, Redux Tools, and Camera Filename Prompt Techniques for Creating or Editing Images in Any Style and Realism

## Authors

- [Zijian Yang](https://www.linkedin.com/in/zijian-yang/) (**ORCID:** [0009-0006-8301-7634](https://orcid.org/0009-0006-8301-7634))

## Introduction to FLUX 1.1

On October 4, 2024, Black Forest Labs launched the latest image generation model, FLUX 1.1 [pro], along with the BFL API, offering advanced image generation capabilities for developers and enterprises. From faster generation speeds to higher image quality, this version is poised to become another milestone in the field of image generation. Here are the key highlights of FLUX 1.1 [pro]:

- **Parameter Scale**: Boasting 12 billion parameters, significantly surpassing similar models.
- **Generation Speed**: Enhanced by **6 times** compared to the previous version, greatly improving efficiency.
- **Resolution Support**: Natively generates ultra-high-definition images up to **2K** resolution.
- **BFL API**: Introduces a new API interface, supporting quick integration of image generation features.
- **Industry Recognition**: Achieved the highest Elo score in Artificial Analysis testing, with performance highly acclaimed.

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/202412110030292.png)

[*https://artificialanalysis.ai/text-to-image*](https://artificialanalysis.ai/text-to-image)

Additionally, Black Forest Labs has open-sourced the FLUX series of tools:

- **FLUX.1 Fill**: An inpainting and outpainting model for partial redraws and image expansion.
- **FLUX.1 Depth & Canny**: The official ControlNet model.
- **FLUX.1 Redux**: Transforms image styles through prompts.

This article will guide you step-by-step through the new FLUX 1.1 AI drawing model and a suite of powerful drawing tools. With just a simple trick, you can remove the "AI smell” from images to achieve photo-level quality, whether for portraits or landscapes. All this can be accomplished with just a few clicks, making it accessible to complete beginners.

You can experience all the latest features by using [FLux.1 AI](https://flux1.ai/), where registering will give you 10 free credits.

## Generating Ultra-Realistic Images with Camera Filename Prompts

This technique is incredibly simple to use. You just need to mimic the file naming format of DSLR cameras in your prompts.

For instance, **“CR2”** is the raw image file format used by Canon cameras. By inputting **“IMG” + a random number + “.CR2”**, along with your desired content, you can create a realistic image.

For example, using “a cute cat” as a prompt, head over to the [FLUX 1.1 AI Image Generator](https://flux1.ai/flux1-1) to experience the latest and most powerful model. You don’t need to worry about anything else—simply paste the prompt, select the image size, and let the AI handle the rest.

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/202412110030065.png)

As you can see, the image is aesthetically pleasing, but there are still noticeable AI-generated styles and unrealistic elements. Now, let's try using the same seed with the addition of a camera filename at the beginning of the prompt:

```
IMG_1018.CR2: a cute cat
```

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/202412110031353.png)

You can see that the photo looks much more realistic.

For example, when we input “selfie on The Great Wall,” the resulting image is already quite close to reality. However, the lighting and the people appear unnatural, and the distant landscape has a noticeable smudging effect.

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/202412110031692.png)

By modifying the prompt to include "IMG_0314.cr2," as in “IMG_0314.cr2: selfie on The Great Wall,” you can see that the image appears significantly more natural and realistic.

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/202412110031203.png)

Using this prompt technique, we can achieve a variety of styles.

### **Vintage Film Style Prompt**

**"IMG_0143.CR2: candid photo of a group of friends at a 1970s outdoor festival"**

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/202412110031172.png)

**"IMG_1018.CR2: vintage black-and-white portrait of a man sitting at a typewriter in an old newsroom"**

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/202412110031691.png)

### **Modern Smartphone Photo Texture Prompt**

**HEIC** is the file format used by Apple for iPhone photos, often characterized by high resolution and clarity typical of modern smartphone photography. By including an extension like **IMG_1025.HEIC** in your prompt, you can generate snapshots that resemble natural photos taken with a smartphone. This filename is particularly effective, with notable results observed using numbers such as 134, 1025, and 2222.

**"IMG_1025.HEIC: a family"**

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/202412110031120.png)

**“IMG_2222.HEIC chinese family”**

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/202412110031854.png)

### **Creating Early Internet Style with Photobucket Find Prompt**

By including a structure like **Photobucket find, IMG_0024.CR2,** in your prompt, you can simulate the style of photos shared on platforms like Photobucket from the early internet era. These images often have slight pixelation and compression artifacts.

**"Photobucket find, IMG_0024.CR2, 2005: a grainy photo of friends at a high school prom"**

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/202412110032068.png)

**"Photobucket find, IMG_0024.CR2, 2006: group of teenagers hanging out at a mall in the early 2000s"**

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/202412110032543.png)

### **Ordinary Everyday Snapshot Prompt**

The **.jpg** extension typically represents compressed image files, making it suitable for generating everyday, less polished snapshots. These images may appear slightly distorted but closely resemble the real-life records of an average person's daily life.

**“IMG_1018.jpg: casual photo of a street vendor in a busy market selling fruits”**

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/202412110032737.png)

**"IMG_1018.jpg: blurry photo of kids playing soccer in a neighborhood street"**

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/202412110032787.png)

### **Additional Extensions and Photography Equipment Prompts**

In addition to CR2, HEIC, and JPG, other formats can simulate the effects of different photography equipment, further enhancing the realism of images.

- **TIFF**: This professional photography format produces higher-resolution images that may exhibit slight graininess, making it ideal for recreating mid-20th century photographic styles.

**"IMG_1120.TIFF: black-and-white portrait of a 1950s jazz musician playing a saxophone"**

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/202412110032285.png)

**"IMG_0456.TIFF: candid street photo of a woman walking in New York City during the 1960s"**

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/202412110033228.png)

- **BMP**: A format used by early Windows operating systems, characterized by lower image quality and slight color deviations, suitable for recreating digital photos from the 1990s.

**"IMG_3345.BMP: photo of a family at a computer desk in 1998"**

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/202412110033894.png)

## FLUX Fill: Inpainting and Outpainting

FLUX Fill is a versatile image editing tool that uses cutting-edge inpainting and outpainting technology. It seamlessly integrates new content into existing images, maintaining a natural and cohesive appearance.

With FLUX Fill, users can extend images beyond their original borders, make precise edits, and even guide modifications using text prompts. These capabilities make it suitable for creative projects and professional workflows requiring high-quality results.

For example, using the FLUX Fill tool, we can transform a cat into a dog in an image. Simply upload the image, and a URL will be provided. Then, use the cursor to erase the cat, leaving a blank space. In the prompt section, enter "A dog on the table," and FLUX Fill will replace the cat with a dog while keeping the rest of the image unchanged.

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/202412110033466.png)

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/202412110034562.png)

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/202412110034905.png)

Alternatively, we can change the background of the image to place the cat on a beach and add sunglasses. First, erase the background around the cat, making it white, and also erase the cat's face. Then, enter the prompt "A cat sitting on the beach wearing a pair of sunglasses." The result will transform the scene accordingly.

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/202412110034625.png)

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/202412110034725.png)

We can even change a person's facial expression, such as transforming a sad face into a happy one.

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/202412110034734.png)

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/202412110040045.png)

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/202412110041406.png)

## FLUX Canny & Depth: Preserve structure while transforming content

FLUX Canny and FLUX Depth are advanced models designed to maintain structural integrity during image edits. FLUX Canny utilizes edge detection to guide transformations, ensuring sharp, detail-oriented edits, while FLUX Depth uses depth maps to preserve spatial coherence, making it ideal for depth-aware tasks.

Both models support text-guided image modifications, allowing for precise retexturing and restyling while keeping the original composition intact.

You can find these two tools here:

[https://flux1.ai/flux-canny](https://flux1.ai/flux-canny)

[https://flux1.ai/flux-depth](https://flux1.ai/flux-depth)

For example, we can use Canny to transform an image of a man running into Iron Man running through a forest.

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/202412110035025.png)

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/202412110035213.png)

The principle of Canny can be understood through the following image, as it primarily captures edge information.

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/202412110035984.png)

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/202412110036994.png)

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/202412110036006.gif)

[*https://huggingface.co/XLabs-AI/flux-controlnet-canny-v3*](https://huggingface.co/XLabs-AI/flux-controlnet-canny-v3)

We can also use the Depth feature to create new images by preserving the depth information of the original. For instance, we can transform a photo of a narrow alley into a cyberpunk world.

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/202412110036281.png)

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/202412110037725.png)

Here's how FLUX Depth works.

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/202412110037162.png)

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/202412110037645.png)

[*https://huggingface.co/XLabs-AI/flux-controlnet-depth-v3*](https://huggingface.co/XLabs-AI/flux-controlnet-depth-v3)

## FLUX Redux

Flux Redux enables users to generate image variations and restyle existing images using text prompts. It maintains the core characteristics of input images while allowing for creative modifications, making it ideal for tasks like variation generation and guided restyling.

You can find FLUX Redux here:
[https://flux1.ai/flux-redux](https://flux1.ai/flux-redux)

For example, if we input a portrait photo, Redux will output a variant image.

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/202412110038270.png)

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/202412110038829.png)

# FLUX LoRA

In addition to the tools mentioned above, we can also use different pre-trained LoRA models to achieve specific styles. For instance, in [**Flux Then And Now**](https://flux1.ai/flux-then-and-now), you can create images with a mix of contemporary and historical black-and-white photo styles using prompts.

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/202412110038603.png)

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/202412110038233.png)

Alternatively, you can generate images in a [Cute 3D Style](https://flux1.ai/flux-cute-3d).

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/202412110038918.png)

Or in a [Minecraft](https://flux1.ai/ai-minecraft) style.

![](https://cdn.jsdelivr.net/gh/data-community-of-practice/AI-Graph-Obsidian@main/img/202412110038236.png)

More style LoRAs and features are waiting for you to explore.

## **Conclusion**

I hope this guide has given you a clear understanding of how to make the most of FLUX 1.1 and its incredible suite of tools. From creating ultra-realistic images with filename-based prompts to exploring styles and edits with FLUX Fill, Canny, Depth, and Redux, the possibilities are endless. Whether you're just starting or looking to push creative boundaries, FLUX 1.1 offers something for everyone. Give it a try, and see what amazing results you can achieve!

## **Source**

- [https://flux1.ai/](https://flux1.ai/)
- [https://blackforestlabs.ai/flux-1-1-ultra/](https://blackforestlabs.ai/flux-1-1-ultra/)