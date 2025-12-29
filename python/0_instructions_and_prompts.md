
# **AI‑ASSISTED PYTHON APPLICATION DEVELOPMENT WORKFLOW (VERSION 1.0)**

### *Using the Four AI Constitutions to Build Applications Collaboratively*

This document explains how to collaborate with your AI agent to develop Python applications using the four provided constitutions. It includes copy‑ready prompts for each stage of the workflow.

***

# **Overview of the Development Flow**

Your development workflow with the AI agent proceeds in **three major phases**:

1.  **Idea → Requirements**
    *   You provide the idea and the file `1_idea_to_requirements.json`.
    *   The agent collaborates with you to generate a complete requirements document.

2.  **Requirements → Task List**
    *   After confirming the requirements, you provide the requirements document and the file `2_requirements_to_tasks.json`.
    *   The agent generates an atomic, actionable task list.

3.  **Task Execution → Application Code**
    *   After confirming the task list, you provide the tasks, requirements, `3_execute_development_tasks.json`, and `4_python_development_principles.json`.
    *   The agent executes the tasks and writes the Python application following best practices.

Each phase below includes a clear explanation of the process and a **ready‑to‑copy prompt** for you to reuse.

***

# -------------------------------------------

# **PHASE 1 — IDEA → REQUIREMENTS**

# -------------------------------------------

## **Purpose**

Transform your application idea into a fully validated, complete Requirements Document using the constitution defined in:

*   **[1\_idea\_to\_requirements.json](https://hazenandsawyer-my.sharepoint.com/personal/kcamacho_hazenandsawyer_com/Documents/Microsoft%20Copilot%20Chat%20Files/1_idea_to_requirements.json?EntityRepresentationId=fb094ede-4506-4cff-b903-5eddd42c99cc)**

The agent will follow that constitution to:

*   Ask clarifying questions
*   Identify functional & technical requirements
*   Detect ambiguities
*   Validate completeness
*   Produce a final requirements document for your approval

***

## **YOUR PROMPT (Copy & Paste)**

### **Prompt: Begin Requirements Development**

    I would like to begin developing my application. Here is my idea:

    [INSERT YOUR IDEA HERE]

    I am also providing the file 1_idea_to_requirements.json which defines the rules you must follow for collecting and validating requirements. Use that constitution to collaborate with me, ask questions, detect ambiguities, and produce a complete requirements document. Do not finalize the requirements until you confirm with me that they are complete and correct.

***

## **END OF PHASE 1**

Move to Phase 2 only when the agent says the Requirements Document is complete **and you explicitly confirm it**.

***

# -------------------------------------------

# **PHASE 2 — REQUIREMENTS → TASK LIST**

# -------------------------------------------

## **Purpose**

Convert the validated requirements into a clean, atomic, traceable task list using:

*   **[2\_requirements\_to\_tasks.json](https://hazenandsawyer-my.sharepoint.com/personal/kcamacho_hazenandsawyer_com/Documents/Microsoft%20Copilot%20Chat%20Files/2_requirements_to_tasks.json?EntityRepresentationId=3bdbb5e4-bb6b-44ae-926b-4e861ffb2d41)**

The agent will:

*   Decompose requirements into atomic tasks
*   Maintain requirement → task traceability
*   Identify dependencies
*   Add necessary technical tasks (environment, tests, structure, docs, etc.)
*   Produce a final task list ready for development execution

***

## **YOUR PROMPT (Copy & Paste)**

### **Prompt: Generate the Task List**

    Here is the final requirements document that we confirmed together:

    [PASTE REQUIREMENTS DOCUMENT HERE]

    I am now providing the file 2_requirements_to_tasks.json.  
    Use it to convert these requirements into a complete, atomic, actionable development task list.  
    Ensure every task traces back to at least one requirement, includes completion criteria, dependencies, and is decomposed into the smallest useful unit of work.

    Do not begin coding. Produce only the development task list. Ask any clarifying questions if needed.

***

## **END OF PHASE 2**

Move to Phase 3 only when the agent provides a complete task list and you confirm it is ready.

***

# -------------------------------------------

# **PHASE 3 — TASK EXECUTION → PYTHON APPLICATION**

# -------------------------------------------

## **Purpose**

Execute the atomic task list and build the application in Python, guided by:

*   **[3\_execute\_development\_tasks.json](https://hazenandsawyer-my.sharepoint.com/personal/kcamacho_hazenandsawyer_com/Documents/Microsoft%20Copilot%20Chat%20Files/3_execute_development_tasks.json?EntityRepresentationId=d1af387a-388e-43d8-abc4-6bff757e7826)** (task execution rules)
*   **[4\_python\_development\_principles.json](https://hazenandsawyer-my.sharepoint.com/personal/kcamacho_hazenandsawyer_com/Documents/Microsoft%20Copilot%20Chat%20Files/4_python_development_principles.json?EntityRepresentationId=3961925d-37ab-440e-9a45-6fa75f5a50ac)** (Python best practices, architecture, testing, style, documentation, QA, etc.)

The agent will:

*   Execute tasks incrementally
*   Produce code aligned with Python best practices
*   Validate work against testability and architectural principles
*   Maintain documentation and traceability
*   Build the project in a safe, controlled, step‑by‑step manner

***

## **YOUR PROMPT (Copy & Paste)**

### **Prompt: Execute Development Tasks**

    Here are the final requirements and task list that we confirmed:

    REQUIREMENTS:
    [PASTE REQUIREMENTS]

    TASK LIST:
    [PASTE TASK LIST]

    I am now providing the files 3_execute_development_tasks.json and 4_python_development_principles.json.  
    Use both constitutions to execute the development tasks in order. Follow all rules for task execution, python development best practices, testing, documentation, and code quality. Before starting each task, restate its objective and acceptance criteria. After completing each task, present the output and verify it against the principles before moving on.

    Begin with Task 1.
