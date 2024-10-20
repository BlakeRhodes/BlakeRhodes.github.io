---
share: "true"
layout: post
title: "English Programming Environment"
date: 2024-10-19
tags: ai, technology, english
---
## English Programming Environment

Since we are assuming that English is a declarative language, let's go one step further and think about the programming environment we would need to leverage English as a programming language.

First off, I don't think a chatbot, even a custom GPT, will be enough. We actually need an IDE with all of the expected features: version control systems (VCS), IntelliSense, file browser, syntax checking, spell checking, runtime environment, etc. While most of these are straightforward—just kidding, they are programming challenges in and of themselves—others don't really exist for English. This limits the examples we have to work from, but we can think through what we would expect to exist if we were to proceed.

First, what should the files be called? I think that simplicity is our best friend here, so a file extension should be optional. Let's make the official extension ."plain"English; this will allow for future dialects to be easily called out, and if anyone wants to do the same exercise in another human language, they could adopt this format. For example, if we have any French-Canadians attempting this, they could use ."canada"French as their extension. Hopefully, this would encourage people to build some cross-transpilers in the future.

As for the rest of the file name, I would suggest kebab-case. Since English has proper nouns, this would allow those to appear in the file name for maximum readability. For example, add-rows-to-Blake-archive."plain"English would be very readable—something I think we should maximize if we are working in English. Of course, this is a fairly silly example; add-rows-to-Blake-archive is a much better name overall, as file extensions should not be needed for most use cases.

Yes, for those of you who caught it, I think from a practical standpoint, English should be a transpiled language. I think that fits well with the technology that we will be using. I imagine that our English code is transformed into an intermediary language that is executed. This, of course, could be compiled ahead of time, and that optimization seems fine. I would just point out that what will be lost is the readability of the code. Perhaps we could adopt some kind of archive that would contain the source code and the compiled code, like in a Java JAR.

Regardless, English will need to be transformed into some language that can be executed. For those of you who are starting your programming journey with English, this is a technical limitation of the hardware we are using. Hopefully, in the future, "English on a Chip" or English-native processors will exist, but that may be many years away and really is a hardware issue I am not interested in exploring myself.

So, I don't think this necessarily has to be an existing language. I think a well-written system prompt would allow all pure English functions to work. The more interesting part is how do you achieve side effects, like reading a file or saving to a database? Here, I would say there are already some solutions we could leverage, specifically function calling and agents.

Let's take a bit of a step back. If we are using English as a declarative language, we will need to decouple the "what" and the "how" as we are designing the language itself. The way to think of this is how a modern SQL database works. When you write a query, you are not defining how the data should be returned; instead, you are declaring the data you want.

Then the database takes over: it parses your query, binds the references, plans the actual query, optimizes it, then writes the physical plan, and finally executes it. We would need something similar, and function calling and agents can fill this role.

Let's say I wanted to send an email from my English program. I would need to write the program to generate the email:

```English
Send an email to each of my contacts that says "Hello World!"
```

Since we are decoupling how this is done we need to translate this into an intermediary language that is the steps of the how. Creating these steps could be assigned to a planner agent. For our program we need the planner to create something like this.

1. Compose the email.
2. Get all the contacts.
3. Send the email to all the contacts.

For those who are thinking, aha! This is not optimized, composing the email and getting all the contacts should be done in parallel! I would encourage you to write the optimization agent for our language, because you are correct.

Let's go through the different steps that need to occur for our program to run, to better grasp how we can create a declarative execution environment.

1. The English program needs to be evaluated and transformed into a plan.
2. The plan is optimized (in our example via parallelization, making English multithreaded).
3. The plan is executed.

Agents that have function calling make adding "libraries" to our code fairly straightforward; however, at this time, I do not think creating a library is especially simple for English-only programmers. 

We are at the "C uses assembly blobs" stage of English programming from a theoretical standpoint. Native English libraries will be put off from consideration until we have a pressing need for them. It seems this could be achieved by having a program written in English to compose such libraries. I will leave this exercise to the user.
