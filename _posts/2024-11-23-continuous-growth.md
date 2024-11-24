---
layout: post
title: Continuous Growth
subtitle: Skilling Up in the Age of AI
date: 2024-11-23
tags:
  - ai
  - reflection
  - technology
share: "true"
---
There's something undeniably exhilarating about being caught off guard by a surprise. Even the tiniest revelations can have an enlightening impact, much like a sudden jolt of dopamine to the brain. I encountered such a pleasant surprise recently when I discovered that one of my colleagues, despite working in the field of AI, had never actually seen a REST API in action.

To me, this was startling. Perhaps it's because I inhabit a technology bubble—actually, that's definitely the case—but even within our sphere, there's an expectation of certain knowledge, particularly when it comes to someone who is adept at navigating co-intelligence and the like. They didn't quite grasp how the system we were building was distinct from the off-the-shelf products we've used before.

I endeavored to clarify the concept for them, and eventually, we reached a point of understanding. It was clear from their newfound enthusiasm and the gears turning in their head that they were beginning to appreciate how these ideas could enhance our offerings. 

To half of my audience, the notion that someone hasn't encountered an API may seem extraordinary. To the other half, who might be inquiring what an API even is, a new horizon has been elevated. The existence of AI is pushing the boundaries of our bubble, equipping more people to accomplish tasks more rapidly and capably. This is a boon, especially considering the formidable challenges humanity faces: pollution, resource scarcity, political strife, and the endless wait for "Star Trek: Section 31" contribute to a collective anxiety that dampens our quality of life.

For those veterans who are surprised by the unfamiliarity with APIs, consider this a form of first contact. Individuals who might previously have ventured no further than social media pages are now beginning to see the interconnectedness of our world, powered by our proverbial "magic rocks full of lightning." 

Historically, the tech world has been somewhat insulated, with rigid gates based on perceived intelligence or skill—a practice we should abandon as AI democratizes technological ability. Talent is now pouring into our domain, not because these individuals were fundamentally different from us, but because they found fulfillment in different feedback loops.

To the rest of my audience, who may feel like interlopers amidst the tech wizards, be aware that as you venture into the bubble, you're joining a community that has traversed this path before. Where you are taking your first steps, they are endeavoring to build "warp drives." But this isn't a call to discouragement—it's an exciting reminder of the empowering shift AI is instigating. As technology natives, we see the sky as the new starting line, not the limit.

I may risk sounding like an old man shaking his fist at a cloud (and I am to be fair), but I implore you not to view AI's offerings as mere shortcuts. These tools are set to become essential for success in a world post-AI assimilation. Yet, remember, there are no "no code" solutions without understanding.

This brings me to thinking about English as a programming language. In a future where expressing your will can bring it to life through a digital swarm, clarity in your instructions is paramount. Let's compare

```English
Make me a good app server.
```

to

```English
Create a good app server like the one described below.

Core Features

First off, it needs to handle all the latest web traffic tech. That means **HTTP/2 and HTTP/3 (QUIC)** for faster, more efficient connections, and **WebSocket support** for real-time updates. Whether it’s hosting REST APIs or the newer GraphQL stuff, it’s gotta be flexible. And for static content—things like images or JavaScript files—it should serve them up blazing fast, maybe even with built-in caching or integration with a CDN.

Oh, and let’s talk microservices. Modern setups often break things into smaller pieces, so the server should help with service discovery and distributed tracing to keep everything playing nice.

Performance and Scalability

This thing needs to scale like a champ. Whether you're running it on one big machine or across a whole cluster, it should handle spikes in traffic without breaking a sweat. It should have asynchronous I/O, so it can juggle thousands—if not millions—of connections efficiently. Add auto-scaling so that when traffic surges, it brings more resources online, then scales back down to save costs.

Plus, edge compute compatibility is big now. That means pushing some of the processing closer to the user (like at a data center near them) for lower latency.


Security

Now, security. You don’t want to worry about someone sneaking in or messing with your app. So, at the very least, enforce LS 1.3 for all HTTPS traffic, and include a built-in Web Application Firewall (WAF) to block common attacks like SQL injection or XSS. Add in rate limiting and DDoS protection, and you’re good to handle abusive traffic.

For APIs, token validation is non-negotiable, and having built-in support for OAuth2 and OpenID Connect ensures everything’s locked down properly. Don’t forget audit logging, so you can see who did what and when.

Observability

Keeping tabs on your server is huge. You want to know how it’s doing at all times, so export metrics to something like Prometheus and make sure you’ve got distributed tracing in place to track what’s happening across services. If anything goes wrong, centralized logs—say, with an ELK stack—help you figure out what happened. Oh, and health checks are a must for stuff like Kubernetes deployments.

Performance Goals

So how fast should it be? Think sub-50ms response times for almost all requests, even when handling a million concurrent users. Modern hardware can do this if your server is efficient. And it should work just as well on a single big machine or a cluster of hundreds.

Compatibility and Flexibility

No one wants to be stuck with a server that only works in one ecosystem. This needs to support all the big programming languages—Node.js, Python, Java, Go, .NET, etc.—and run in containers like Docker. It should also slot perfectly into Kubernetes setups.


Deployment and Management

Let’s make deployment smooth. Use CI/CD pipelines like GitHub Actions to push updates without downtime. For configuration, stick to something declarative—YAML or JSON works great—and integrate with tools like HashiCorp Vault for managing secrets securely.

The Extras

Looking ahead, this server could evolve to support stuff like machine learning inference directly or even some lightweight *erverless functions for quick, on-demand computing. As edge computing grows, having more features optimized for local processing could make it a real game-changer.
```

Now clearly this an exaggeration, but I am trying to illustrate that really understanding the technology and how it works translates to even better prompts. The first one may result in a fine system, however the second one makes the exact system that will fit the bill. AI is not a substitute for knowledge, so continue to gain knowledge of the new bubble you have joined.

Luckily, AI is a great teacher. If you are part of the audience that doesn't know what an API is, or have some idea but it mostly just a term that have been thrown around, use this prompt to learn more.

```English
Teach me about APIs in the context of computer systems, focus on REST APIs. Go step by step, I am trying to learn this and the concept is new to me.
```
