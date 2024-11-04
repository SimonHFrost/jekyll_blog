---
layout: post
title: "Unleash Midjourney's magic... A creative workflow for themed image generation"
image: /assets/midjourney/arrow/lamington-arrow.jpg
---

Generative AI is transforming creative digital design. Identifying and optimising workflows with existing AI tools are essential for staying ahead of rapid developments in the field 📈.

In this blog post, I'll share my workflow to create consistently stylised assets with Midjourney featuring my favorite New Zealand deserts. This workflow can be used throughout digital design from storyboarding, stock image generation, icons, and much, much, more... ✨

<img src="/assets/midjourney/arrow/jaffa-arrow.jpg"/>
<div style="margin-bottom: 8px"/>
<img src="/assets/midjourney/arrow/lamington-arrow.jpg"/>
<div style="margin-bottom: 8px"/>
<img src="/assets/midjourney/arrow/pavlova-arrow.jpg"/>

## 1) Seed a consistent style prompt

To ensure a consistent theme between images... you need consistent prompts. Crafting a prompt that's stylistically specific, yet general enough to cover your subjects can be difficult if you don't have prompt engineering experience. That's where your favorite LLM (Claude, ChatGPT) can help!

Input:

<div class="code-block">
Prepare a midjourney prompt for an image of a pink New Zealand lamington, cartoon style modern, funky, and trippy. The aim is to come up with a style I can use with different reference images to convey a theme.
</div>

Prompt:

<div class="code-block">
Pink New Zealand lamington, cartoon-style illustration, vibrant neon colors, surreal distortions, geometric patterns, swirling psychedelic backgrounds, bold outlines, exaggerated proportions, abstract shapes, retro-futuristic elements, liquid textures, kaleidoscopic effects
</div>

## 2) Tweak your prompt

<img src="/assets/midjourney/arrow/trippy-arrow.jpg"/>

A LLM should get you to a good stylistic starting point, but you'll have to adjust until you get something close to your target aesthetic. Mine ended up being… a bit too bizarre for me, and in my case meant removing abstract references and adjusting some terminology:

<div class="code-block">
Cartoon-style illustration of a pink New Zealand lamington, vibrant color palette, playful geometric shapes, funky patterns, bold outlines, slightly exaggerated proportions, retro-inspired elements, smooth gradients, dynamic composition
</div>

## 3) Upload reference images

I find Midjourney isn't great with specifics. I had exact positioning in mind, and although the technology is constantly improving, prompts like 'on the left side' or using specific colors can be a surprising challenge.

Since I knew exactly how I wanted the subject to be positioned, I did a quick sketch:

![Sketch Cube](/assets/midjourney/sketch-cube.jpg)

I included the lined paper as it could add an interesting stylistic element. Ultimately this is a creative workflow, which often requires creative solutions!

The new Midjourney web platform (<a href="midjourney.com">Midjourney.com</a>) is a lot more accessible compared to the original Discord. One of the benefits is that it is super easy to upload images with an icon directly in the search area.

<img src="/assets/midjourney/add-image-small.png" />

## 4) No cream please! (Optional)

Midjourney was fixated on generating a Lammington with a cream dolop on the top, and while a lammington <i>has</i> cream, it's not a visual feature.

![Cream](/assets/midjourney/cream.png)

This is where mastery of the Midjourney API comes in, with <span style="background-color: black; color: white; font-family: monospace; padding: 4px;">--no cream</span> we can tell Midjourney to exclude specific items.

<div class="code-block">
Cartoon-style illustration of a pink New Zealand lamington, ... --no cream
</div>

Midjourney is a powerful tool and there are a range of similar commands that are worth exploring via the documentation and Youtube if you're serious about improving your prompt engineering skills.

## 5) Iterate!

The key to good generated assets are the variations along the way! I often find that Midjourney gets close… but you might not know what is lacking. That's where variations come in!

<img style="margin: auto; display: block;" src="/assets/midjourney/vary.jpg"/>

Choose one of the four images that it gave you back and iterate! Clicking iterate in the bottom right hand ‘Creation Actions’ menu will give you four resulting options.

Use upscale when you’re happy with what you want, and want a higher resolution.

<img style="margin: auto; display: block;" src="/assets/midjourney/upscale.jpg"/>

Also try experimenting with your prompt! Remove or add sections that don’t align with your vision. In my case, Midjourney got close with a lammington representation, but I didn't want any cream.

## Conclusion

Generative AI tools like Midjourney lower the barrier of digital design by offloading creative workflows to AI. Identifying and optimising these workflows are the key for staying ahead in the rapidly changing AI landscape.

The new Midjourney.com webapp makes difficult tasks easier with more intuitive access to common operations like adding reference images, generating variations, and upscaling.

I hope you find this workflow useful!
