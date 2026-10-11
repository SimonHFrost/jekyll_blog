---
layout: post
title: "Building a voice agent"
description: "What building a coaching assistant taught me about design, verification, and faster feedback loops with coding agents."
image: /assets/building-a-voice-agent/voice-conversation.png
draft: true
noindex: true
---

![A person speaking into a flowing voice interface](/assets/building-a-voice-agent/voice-conversation.png)

Are you a software engineer in 2026 if you haven’t built a chatbot? This year I worked with a client to build a coaching assistant. It highlighted how my process building software has changed since using coding agents, and why design, verification, and loops are more important than ever.

## Design is more important than ever...

![A hand drawing a path through a changing landscape](/assets/building-a-voice-agent/design.png)

Product Requirement Documents (PRDs) are useful to capture the intent behind what you want to build. Traditionally they’re great for communicating between larger teams and stakeholders, now also surprisingly good at communicating to your coding agent.

There’s no single best format for PRDs. It should capture the needs of your users: what is the problem you’re trying to solve? And what’s your proposed solution?

PRDs are a perfect time to identify your biggest unknowns and critical components. What are the biggest assumptions you have, and what if it’s not what you expect? If you don’t know the answers to this, howour agent to?

I was building a coaching agent for a client, so I was worried about latency: if the chatbot didn’t respond quickly enough the experience would suddenly not feel ‘conversational’ and unusable. We also wanted to iterate on UX around transcription and confirmation.

## Verification is more important than ever...

![A magnifying glass inspecting the result](/assets/building-a-voice-agent/verification.png)

Coding agents have drastically sped up building, verification is even more important! If you can’t get quick, reliable feedback, then you lose with open PRs, or SLOP. For us this meant daily TestFlight releases, and a simple way to report and track feedback.

One hack is to de-couple verification steps from your regular build cycle. Configuration like the coaches’ system prompt was dynamically loaded externally so the team was able to verify behaviour without waiting for another release. We used langfuse.com’s ‘Prompt Management’ feature to load this.

## Loop optimisation...

Once you have your designing and verification

Having a human centered product… ude the human a lot. Once you have your designing and verification nailed, you can start laser focusing on your UX loop: designing changes and verifying they’re intuitive.

Our main focus was to ensure voice conversations felt natural, and text/voice UX made sense. So what better way than involving the coach in testing. Voice technology was changing quickly as LLMs have recently gained a lot of attention.

![An infinity loop circling a gear](/assets/building-a-voice-agent/feedback-loop.png)

Conversational AI is broken down at different stages, this introduced latency at each step, and because of the long pauses which felt unnatural. There are three stages involved in getting a response to the user: STT > LLM > TTS. Each of these had latency at the start and the beginning.

Having control of every stage is powerful. Originally we used iphone transcription to Claude to openAI whisper, but realtime api came out: https://developers.openai.com/api/docs/models/gpt-realtime. Realtime api superior, but can’t customise different parts of stack. Direct Input audio > output audio

This loop is the same process as before, but moves a lot faster with coding agents…

## Conclusion

The rules of building elegant software haven’t changed. Design and Testing have just become more important.

![A diagram showing how coding agents shorten the build stage](/assets/building-a-voice-agent/build-speed.png)

Using coding agents to build lets you focus on what’s important to your users and client. Tools like Langfuse provided a toolkit for composing prompts and tracking agent calls. The software engineering process is still largely unchanged, but increased speed
