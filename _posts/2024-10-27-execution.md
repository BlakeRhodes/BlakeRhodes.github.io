---
layout: post
title: Execution Agent
tags:
  - ai
  - eee
  - execution
  - english
date: 2024-10-27
share: "true"
---
	# Execution Agent
	
	The Execution Agent is at the heart of executing programs in our system. Its role is simple but vital: to take a program and make sure it runs as expected. To do this, it needs access to specific tools, and which tools it needs will depend on how the overall system is structured. So, let's pause and think through the fundamentals of how our system should work before diving too deeply into the agent's specific functions.
	
	# Key Assumptions
	
	Our approach assumes that:
	- **The system is distributed**
	- **The system uses Event-Driven Architecture (EDA)**
	- **The system is modular**
	
	These assumptions help us create a more flexible, powerful setup that can scale and adapt to various demands. Each assumption brings some benefits and helps us address different needs of the system. Here’s a breakdown of each assumption and the reasoning behind it:
	
	## Distributed System
	
	In today’s computing world, most complex systems are divided into subsystems, each with a specific role. This distribution of components lets us mix and match services to support different workflows and builds resilience—no single part depends solely on a single machine or service. Distributed systems allow for more robust setups and let us spread the load across many machines or environments.
	
	## Event-Driven Architecture (EDA)
	
	EDA is a method for organizing code that fits well with distributed systems, especially those built on our declarative, English-as-a-Programming-Language (EaaPL) model. EDA revolves around responding to “events” like actions or requests as they happen. For example, when you get a new email or a button is clicked, those are events. By organizing our system to respond to events, we can easily add features like logging and debugging since we’ll always know what triggered any action.
	
	## Modularity
	
	A modular system has a couple of major benefits, but here, security is the standout. By modularizing our code, we can limit which parts of the system have access to sensitive information or actions. We do this by creating an allowlist—a list of specific tools or permissions that each module has. For instance, an email-sending module might be able to send emails but not access user data. This modular approach lets us expand the system with new features by adding new modules without worrying about them having unchecked access.
	
	---
	
	# Execution Agent Walkthrough
	
	The Execution Agent’s main role is to manage program execution by “provisioning” a worker—basically, assigning a worker to do the job. Once a program is done running, the agent will “release” the worker, freeing it up for other tasks. In simpler terms, it’s like assigning a person to a task and then letting them go once it’s completed. This approach also lets us add more workers if the workload grows, making the system scalable.
	
	The agent has other responsibilities, too. It listens for errors or issues that might pop up while a worker is handling a task. If something goes wrong, the agent will try to fix the issue, retry the task if needed, and report any persistent problems back to the system. If the agent is designed well, it could also assign tasks to workers in locations that improve performance, like nearby servers.
	
	Each worker follows a specific “plan” made up of steps. For example, let’s say you want the system to:
	
	```english
	Send an email to all my contacts that says "Hello World!"
	```
	
	Here’s how the steps in that plan might look:
	
	```plan
	a. Get all contacts
	b. Compose Email message: "Hello World!"
	c. Send emails (requires steps a and b)
	```
	
	For each step, the worker publishes an “event” to the system. First, it might ask for the list of contacts, then create the message, and finally send the emails once the information is ready. Each step triggers the next, allowing the worker to get information as it’s needed.
	
	Since this is an event-driven system, the worker can “subscribe” to events that give it the information for each step. This way, it knows exactly when a step has been completed and can move on to the next one. This “subscribe and wait” approach makes the system highly efficient and responsive.
	
	### Handling Errors
	
	Errors are a natural part of any system, and the worker should be equipped to handle most of them. But, sometimes, more significant problems need special attention. For example, a worker might “fail” if it doesn’t receive a response in time or if it’s overwhelmed. When this happens, the agent can report the issue to other parts of the system so they can respond. Error handling deserves its own discussion, but this setup ensures that problems don’t stall the system. The right checks keep things moving smoothly, even when issues arise.
	
	This modular, distributed, event-driven setup helps us build a system that scales, adapts, and securely manages its resources. And it’s a robust foundation for English-as-a-Programming-Language, making programming more intuitive and accessible. 
