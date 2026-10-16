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

Are you a software engineer in 2026 if you haven’t built a chatbot? This year I worked with a client to build a coaching assistant. It showed how my process building software has changed since using coding agents, and why design, verification, and the loop that ties them together is the key.

## Design is more important than ever...

Product Requirement Documents (PRDs) are useful to capture the intent behind what you want to build. Traditionally they’re great for communicating between larger teams and stakeholders, now they're also surprisingly good at communicating with your coding agent.

There’s no single best format for PRDs, and is often organisation specific. It should capture the needs of your users: what is the problem you’re trying to solve? And what’s your proposed solution?

Prototypes with claude design or Lovable are also great at communicating UX interactions that are hard to define with text or diagrams.

![A hand drawing a path through a changing landscape](/assets/building-a-voice-agent/design.png)

This is a perfect time to identify your biggest unknowns and critical components. What are the assumptions you have, and what if it’s not what you expect? If you don’t know the answers to this, how do you expect your agent to?

For my coaching chatbot, I was worried about latency: if it didn’t respond quickly the experience would feel unnatural and unusable. We also wanted to iterate UX around transcription and input modes.

## Verification is more important than ever...

![A magnifying glass inspecting the result](/assets/building-a-voice-agent/verification.png)

Building has drastically sped up so verification is even more important! If you can’t get quick, reliable feedback, then you drown in open PRs, or commit SLOP. For us this meant daily TestFlight releases, and a simple way to report feedback in Notion and screenshots.

Plus points if you can de-couple verification steps from your regular build cycle. Separating the coaches’ system prompt so the team was able to verify behaviour without waiting for another release, meant it kept our verification lean. We used langfuse.com’s ‘Prompt Management’ feature to dynamically load this.

## Looping design and verification...

Shipping human focused software means you need to... include the human a lot. Once design and verification are nailed, spin that loop and get building!

Our focus was to ensure chat interactions felt natural, and text/voice UX made sense especially as technology around voice and chat UX was improving quickly.

![An infinity loop circling a gear](/assets/building-a-voice-agent/feedback-loop.png)

Conversational AI can be split into three distinct stages: STT > LLM > TTS. While it's powerful to control each step of the process, during our verification the long pauses felt unnatural. Each stage runs sequentially and has latency at the start and the beginning which made responses sluggish.

We originally used iphone transcription to Claude to openAI whisper

Realtime api came out: https://developers.openai.com/api/docs/models/gpt-realtime. Realtime api superior, but can’t customise different parts of stack. Direct Input audio > output audio

This loop is the same process as before, but moves a lot faster with coding agents…

## Conclusion

The rules of building robust software haven’t changed, you're still signing your name against code changes you ship to production.

![A diagram showing how coding agents shorten the build stage](/assets/building-a-voice-agent/build-speed.png)

Spinning the loop faster means you can iterate more and focus on what’s important to your users. Drastically increased build speed means the focus now shifts to the edges: Design and Verification.
