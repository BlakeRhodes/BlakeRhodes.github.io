---
share: "true"
layout: page
title: Status
---

1. **User Interface (UI)**: JavaScript (React, Vue) for the front end, and HTML/CSS.

   - **MVP Capabilities**:

     - Simple form for user input handling (used for reminder, weather, to-do tasks, chatbot questions, and sensitive data access requests)
     - Basic rendering of static and dynamic content
     - Minimal responsive design
     - Basic state management
     - Simple integration with a backend API


2. **UI Designer (UID)**: Python or JavaScript for adjusting interface elements dynamically.

   - **MVP Capabilities**:

     - Basic UI adjustment (e.g., form field visibility based on program requirements)
     - Simple component customization
     - Integration with a basic design system

 
3. **Planner**: Python for NLP tasks and plan evaluation.

   - **MVP Capabilities**:

     - Simple natural language command parsing (used for identifying tasks such as reminders, weather checks, to-do list operations, chatbot questions, and sensitive data access requests)
     - Basic task decomposition
     - Simple execution plan creation

 
4. **Evaluator**: Python for evaluation tasks, ensuring plans meet objectives and constraints.

   - **MVP Capabilities**:

     - Basic validation of execution plans (e.g., verifying parsed reminder time, weather request validity, chatbot input, or sensitive data request)
     - Simple feedback generation (e.g., notifying if input commands are not understood, or if access requests require further approval)

 
5. **Executor**: Python for executing planned tasks with concurrency support.

   - **MVP Capabilities**:

     - Basic task execution (e.g., scheduling reminders, fetching weather data, managing to-do list items, handling chatbot requests, processing sensitive data access)
     - Simple concurrency with threading (e.g., handling multiple user requests simultaneously)
     - Basic error handling

 
6. **Capabilities (Side Effects)**: Python, integrated for specific system commands.

   - **MVP Capabilities**:

     - Execute simple system-level commands (e.g., sending notifications for reminders, approving sensitive data access)
     - Security checks for command execution (e.g., verifying user identity for database access requests)

 
7. **Insights (Intelligence)**: Python with AI models (like PyTorch).

   - **MVP Capabilities**:

     - Integrate a pre-trained model for basic insights (e.g., analyzing user input patterns, responding to chatbot queries, and assessing data access requests)
     - Simple data analysis from user inputs (e.g., identifying frequently requested reminders, questions, or sensitive data requests)

 
8. **HitL Terminal**: WebSocket-based terminal, using Python's Flask-SocketIO.

   - **MVP Capabilities**:

     - Basic command-line interface for user input (e.g., manually entering reminder, weather, to-do commands, sensitive data requests, or chatbot queries)
     - Simple WebSocket communication
     - Human-in-the-loop approval interface (e.g., approve or deny access to sensitive databases and monitor chatbot-generated information)

 
9. **Info Layer, Queries, Commands, Data**: SQLite for local prototyping.

   - **MVP Capabilities**:

     - Store and retrieve basic data (e.g., to-do list items, reminder schedules, sensitive database records, chatbot conversations)
     - Simple command processing (e.g., CRUD operations for to-do list, handling sensitive data access requests, storing chatbot interactions)

 
10. **Execution Agent**: Central component responsible for managing program execution.

    - **MVP Capabilities**:

      - Basic worker provisioning (e.g., assigning tasks such as fetching weather data, scheduling reminders, handling chatbot queries, processing sensitive data access)
      - Simple task assignment
      - Basic error detection

 
11. **API for UI Interaction**: REST API to facilitate communication between the UI and backend components.

    - **MVP Capabilities**:

      - Basic RESTful endpoints for CRUD operations (e.g., create, read, update, delete tasks in to-do list, handle chatbot queries, approve sensitive data access)
      - Integration with Planner, Evaluator, and Executor
      - Simple JSON response handling
      - Authentication for basic security

 
12. **Infrastructure**: The underlying system and technologies needed to support the components for a local prototype.

    - **MVP Capabilities**:

      - **Local Server**: Host services on a local machine.
      - **Containerization**: Docker for packaging services.
      - **Orchestration**: Docker Compose for managing services locally.
      - **Logging**: Basic logging with Python's logging module.
      - **Networking**: Simple localhost communication.
      - **Security**: Basic authentication for local access.

 
13. **Event-Driven Architecture (EDA) Components**: Simplified for local processing and testing.

    - **MVP Capabilities**:

      - Basic event producer and consumer setup (e.g., generating events for reminders)
      - Lightweight message broker (e.g., RabbitMQ) for local message passing

    - **Libraries and Tools for EDA**:

      - **Event Broker**: RabbitMQ for local message queuing.
      - **Asynchronous Task Management**: Celery (Python) for simple task queues.
      - **Integration**: Flask for basic REST APIs.
      - **Monitoring**: Simple logging with Python's logging module.

 
14. **Basic English Language Programs for Prototype**:

    - **Program 1: "Remind Me"**

      - Users can input a simple reminder (e.g., "Remind me to take a break in 30 minutes").
      - The system parses the input, schedules a task, and uses the Execution Agent to trigger a notification after the specified time.

    - **Program 2: "Weather Check"**

      - Users can ask for the current weather (e.g., "What's the weather like today?").
      - The system queries a mock weather API or local data source and returns a basic weather update to the user interface.

    - **Program 3: "To-Do List Manager"**

      - Users can add, view, and delete tasks in a simple to-do list (e.g., "Add 'buy groceries' to my to-do list").
      - The system manages tasks in a local SQLite database and interacts with the UI through the API for CRUD operations.

    - **Program 4: "Sensitive Database Access via HitL Terminal"**

      - Users can request access to a sensitive database (e.g., "Access customer data records").
      - The system processes the request, but requires a human-in-the-loop (HitL) to approve the access before any sensitive data is retrieved.
      - The HitL Terminal allows a designated user to manually approve or deny the database access request, ensuring secure handling of sensitive information.

    - **Program 5: "Ask a Chat Model"**

      - Users can ask a general question (e.g., "What is the capital of France?").
      - The system forwards the question to a pre-trained chat model, which processes the input and generates an appropriate response.
      - The response is returned to the user interface for display.