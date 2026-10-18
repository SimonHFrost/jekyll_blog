---
layout: post
title: "Building a voice agent"
description: "What building a coaching assistant taught me about design, verification, and faster feedback loops with coding agents."
image: /assets/building-a-voice-agent/voice-conversation.png
draft: true
noindex: true
sitemap: false
---

<style>
@media (min-width: 769px) {
  .post-content img {
    width: 75%;
    display: block;
    margin-left: auto;
    margin-right: auto;
  }
}
</style>

![A person speaking into a flowing voice interface](/assets/building-a-voice-agent/voice-conversation.png)

Are you a software engineer in 2026 if you haven’t built a chatbot? This year I worked with a client to build a coaching assistant. It showed how building software has changed with coding agents, focusing on the build loop, and why design, verification are more important than ever...

## Design is more important than ever...

Product Requirement Documents (PRDs) are useful to capture the intent behind what you want to build. Traditionally they were great for communicating between larger teams and stakeholders, now they're surprisingly good at communicating with your coding agent.

There’s no single best format for PRDs, and is often organisation specific. It should capture the needs of your users: what is the problem you’re trying to solve? And what’s your proposed solution?

Interactive prototypes with claude design or Lovable are also great at communicating UX interactions that are hard to define with text or diagrams.

![A hand drawing a path through a changing landscape](/assets/building-a-voice-agent/design.png)

Design is a perfect time to identify your biggest unknowns and critical components. What are the assumptions you have, and what if it’s not what you expect? If you don’t know the answers to this, how do you expect your agent to?

For my coaching chatbot, we were worried about latency: if it didn’t respond quickly the experience would feel unnatural and unusable. We also wanted to experiement with input UX and different input modes.

## Verification is more important than ever...

![A magnifying glass inspecting the result](/assets/building-a-voice-agent/verification.png)

Building has drastically sped up so verification is even more important! If you can’t get quick, reliable feedback then you drown in open PRs or commit SLOP. For us this meant daily TestFlight releases, and a simple way to report feedback in Notion with screenshots (basic is better).

One building hack we found was de-coupling verification steps from our regular build cycle. Separating the coaches’ system prompt meant we could verify behaviour without waiting for a release. This meant it kept our verification lean. We used langfuse.com’s ‘Prompt Management’ feature to dynamically configure this.

## Looping design and verification...

Shipping human focused software means you need to... include the human a lot. Once design and verification are nailed, spin that loop and get building!

Our focus was to ensure chat interactions felt natural, and text/voice UX was intuitive. Technology with voice and chat UX has been improving rapidly, and we wanted to find the best solution.

![An infinity loop circling a gear](/assets/building-a-voice-agent/feedback-loop.png)

Conversational AI can be split into three distinct stages:

[STT > LLM > TTS]
Apple Transcription, LLM Claude, and TTS OpenWhisper.

While it's powerful to control each step of the process, during our verification the long pauses felt unnatural. Each stage runs sequentially and has latency at the start and the beginning which made responses sluggish.

During building, OpenAI release their Realtime api (https://developers.openai.com/api/docs/models/gpt-realtime). We quickly realised this API was superior. You can’t customise different parts of stack, but the performance improvements going from direct Input audio > output audio and ease of setup won us over quickly.

Optimising the design/verification loop with features like these is the same process as before, but it moves a lot faster with coding agents so it pays to keep attention.

## Conclusion

The rules of building robust software haven’t changed, you're still signing your name against changes you ship to production.

![A diagram showing how coding agents shorten the build stage](/assets/building-a-voice-agent/build-speed.png)

Building has increased so fast that the spinning loop faster means you can iterate more and focus on what’s important to your users. Drastically increased build speed means the focus now shifts to the edges: Design and Verification.
