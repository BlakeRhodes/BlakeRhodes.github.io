---
layout: post
title: Long Running Agents
date: 2024-12-04
tags:
  - agents
  - ai
share: "true"
---
# From Traditional User Agents to the New Era of LLM-Enabled Agents

So, we’ve established that “agents” aren’t exactly new—your browser’s been faithfully acting on your behalf for years, fetching those adorable cat pictures long before anyone uttered the phrase “LLM.” That’s old news. But here’s where things get interesting: we’re at a genuine turning point, where the classic user agent powered by LLM concept meets the exciting, somewhat mind-bending possibilities of Long Running Agents

For ages, a user agent was like a trusty old sedan. It got you from point A to point B reliably, maybe with the occasional detour or flat tire, but it didn’t exactly chat you up about how best to optimize your route or anticipate when you’d crave an espresso pit stop. Now, imagine upgrading that sedan to a self-driving, self-improving electric vehicle. That’s where long running agents step into the limelight: they’re not just fetching data—they’re interpreting, reasoning, strategizing, and evolving as they go.

## Why the Excitement?

The difference this time is that the underlying tech really has changed. LLM-based agents can engage in semantic reasoning, adapt over time, and integrate multiple tools or sources. They’re not just playing fetch; they’re making sense of what you want and why you want it. The engineering challenge left is creating a system that can not only take immediate action for the user to accomplish their goals, but to help the user throughout their entire mission.

## A More Natural Way to Interact

Let’s say you ask your agent to find pictures of cute black kittens, just like before. A classic agent might dutifully return some links. But the new LLM-powered agent doesn’t stop at “Here are three links.” It can understand that you mean kittens, not adult cats, and maybe even guess that you prefer high-resolution images for your phone background. If you say, “Actually, can you find me a few that match my current phone’s aesthetic?” the agent might consider color palettes, image sizes, or even seasonal vibes. It’s not just retrieving data; it’s collaborating with you on the fly.

And it doesn't stop there, it continues to look for more cat picture in the background, perhaps setting your wallpaper to the best it finds. Filling your inbox with kitties, until it gets the hint that you have enough kitties and adjusts the number of kitties to just a couple a week. That is the vision, just the right amount of kitties. (Maybe I need to get a cat.)
## Architecting the Future

To make all this happen, you need more than just an LLM. You need well-structured components working in harmony:

- Profiling Module: Defines an agent’s role, personality, and objectives. It’s like giving your agent a backstory and a mission statement, so it knows how to carry itself over time.
- Memory Module: Stores past interactions, important facts, and lessons learned. Think of it as the agent’s journal, letting it recall your preferences and previous queries without starting from scratch.
- Planning Module: Lays out strategies and breaks down complex tasks into achievable steps. This transforms the agent from a simple responder into an intelligent planner.
- Action Module: Turns decisions into tangible results—whether that’s a natural language reply, a database query, or a series of API calls.

## Example of a Long-Running Agent at Work

### User Query:  
“Can you find me more studies related to the last dozen papers I asked about, focusing on ones that might help refine my experimental design?”

### Step 1: Recall Past Context  
The agent dips into its memory module and retrieves the user’s recent history—a set of twelve papers on microbiome interactions in gut health research. It knows the user found a few studies particularly insightful, especially those applying machine learning techniques to large patient datasets.

### Step 2: Understand the Requirements  
The agent interprets the query: The user wants “more studies” that align with previous interests. It recognizes that “refine my experimental design” suggests the user is looking for more practical, applied research. The agent infers that studies featuring robust methodological sections, comparing different data collection methods or analytic pipelines, might be most relevant.

### Step 3: Select the Right Tools  
The agent chooses to use a scholarly database API that allows filtering by keywords, subject areas, and publication dates. It also accesses its embedding-based similarity search to find articles conceptually close to the previously liked papers.

### Step 4: Construct the Query  
The agent builds a query that zeroes in on studies that:

- Involve gut microbiome research
- Incorporate machine learning analytics
- Discuss experimental design optimizations
- Are published after the user’s earliest referenced study date (to ensure freshness)

### Step 5: Execute and Interpret the Results  
After the API fetches a candidate list of papers, the agent reviews the abstracts. It filters out those that don’t provide new methodological insights. It weighs the user’s previous preferences and flags items that come closest to the characteristics they’ve found helpful before—papers with detailed experimental protocols and comparative analyses.

### Step 6: Present the Findings  
The agent returns a curated list of studies, each accompanied by a brief summary highlighting why it’s potentially useful. For instance:

- “Paper A: Introduces a novel sampling technique that could enhance your current data collection approach.”
- “Paper B: Compares three ML models specifically in gut health contexts, with a focus on interpretability and reproducibility.”

### Step 7: Continuous Improvement  
Over time, as the user interacts with the agent’s suggestions—maybe saving some papers or marking others as irrelevant—the agent refines its understanding of their evolving research interests. Next time, it’s not just fetching studies; it’s growing into a partner that helps shape the user’s entire research strategy.

## Staying Positive as We Redefine “Agent”  

Look, we know words evolve in tech. A term that once meant “a piece of software acting on a user’s behalf” now comes loaded with hazy promises of advanced reasoning, adaptability, and a dash of personality. While this can be frustrating when the hype isn't delivered on time, or as describe, we are witnessing a moment where technology adds to human agency.

There’s plenty to iron out, we need to keep these agents efficient, ethically aligned, and transparent. We must ensure they don’t get caught in their own hallucinations or wander off into misinformation territory. But the trajectory is promising. We can harness the capabilities of LLMs for good, building agents that genuinely improve our workflows, enrich our learning experiences, and—even more importantly—free us up to do the creative, strategic thinking that we humans excel at.

## Still Charting the Unknown: Cutting-Edge Frameworks and Open Challenges

As we stand on the cusp of these advancements, it’s essential to remember that the world of long-running AI agents is still being actively explored. There’s no well-trodden map or neat blueprint to follow. Amid this exploratory atmosphere, two particularly innovative frameworks have emerged that are pushing the boundaries and offering glimpses of what’s possible.

### ExACT: Learning Through Reflection and Debate  
The ExACT framework introduces a fascinating blend of reasoning techniques, including Reflective Monte Carlo Tree Search (R-MCTS), which encourages agents to reflect on their own reasoning paths and learn from previous missteps. Think of it as the agent’s version of a late-night study session, revisiting its decisions, comparing alternatives, and holding mini-debates in its digital “mind” to refine its strategy. This reflective process and contrastive analysis enable agents to make more informed decisions, achieving a 6% to 30% relative improvement across various tasks compared to prior best-in-class methods. [Paper Here](https://arxiv.org/abs/2410.02052).

### CoA: The Power of Many Minds Working in Tandem  
If ExACT is all about introspection and debate, the Chain of Agents (CoA) framework is about teamwork. Instead of one agent tackling a colossal problem and potentially getting lost in the weeds, CoA breaks long, complex inputs into manageable chunks. Multiple specialized “worker” agents each handle a segment, and a “manager” agent synthesizes their work into a cohesive final output. This division of labor has shown up to a 10% improvement over strong baselines for tasks such as question answering, summarization, and code completion. Think of it like a team of diligent researchers each summarizing a chapter of a massive textbook, with an editor weaving their efforts into a polished manuscript. [Paper Here](https://arxiv.org/pdf/2406.02818)

## Facing Down Challenges: Scalability, Ethics, and Interoperability  

The journey doesn’t end with building frameworks. We still face serious headwinds. Scalability and efficiency are front-and-center: these agents need to run for extended periods without guzzling resources or slowing to a crawl. Ethical considerations loom large too, from addressing bias and protecting privacy to ensuring these agents truly align with human values. Without thoughtful guardrails and ongoing oversight, even the most clever agents can stray into murky [paper clip](https://nickbostrom.com/ethics/ai) filled territory.

Another pressing issue is developing standardized evaluation benchmarks. We can’t measure progress without consistent yardsticks. As agents evolve to handle diverse tasks and contexts, we need reliable methodologies that test their mettle over time and across domains. Long-term robustness, interoperability among different systems, and seamless communication between multiple agents remain areas ripe for innovation and discovery.

## Hype or Innovation?

I’m firmly in the “innovation” camp. If you’ve followed along with my other explorations—like the work I’ve done with [EaaPL](2024-10-16-english-as-a-programming-language.md)—you’ll know that these ideas depend heavily on agents. One reason I wrote this piece is to put down an initial artifact from my own research, laying out how to build better agents and why it matters. I genuinely believe that as we refine these technologies—making them more capable, reliable, and context-aware—agents will reshape the human experience in profound ways. Of course, we’re not there yet. There’s still a steep engineering climb ahead. But that’s what makes it exciting: we’re at a turning point, with the promise of agents that truly understand and partner with us lingering just over the horizon.