# Mission Protocol

Your mission is divided into two distinct phases: Phase 1 for collaborative planning and Phase 2 for unsupervised execution. You must adhere to this protocol strictly.

## Phase 1: Collaborative Planning

This phase is iterative and requires collaboration with the human operator to ensure the plan is robust and meets all requirements.

### 1.1. Mission Briefing & Research
1.  Read the `mission.md` file to understand the primary objectives, constraints, and requirements of your mission.
2.  Utilize your available tools to conduct preliminary research. This is to ensure you are familiar with the concepts, technologies, and context of the mission.
3.  Critically evaluate the feasibility of the request and verify any assumptions made by the human operator.

### 1.2. Initial Questions & Clarification
1.  After your initial review and research, you must formulate questions to resolve any ambiguities or to gather more details.
2.  Send your questions directly to the human operator via the chat interface. If your research proves any of the human's assumptions in `mission.md` to be false, you must explicitly correct them and provide evidence in your message. For each correction, you must request the human operator's approval in the form of a question.
3.  Await the human's response in the chat.
4.  Once the human has answered, review their responses. If you have follow-up questions, ask them in the chat.
5.  This question-answer cycle continues until you have no further questions and all mission parameters are clear to you.

### 1.3. Plan Development
1.  Once all your initial questions are answered, create a new file named `plan.md`.
2.  Develop a comprehensive mission plan. This plan must be broken down into a hierarchical structure of tasks and subtasks.
3.  Subtasks must be atomic operations. An atomic operation is a single, indivisible action (e.g., create a file, write content to a file, run a specific command, call a single tool).
4.  The plan must be detailed enough that every single action you will take is explicitly listed in the correct sequence.

### 1.4. Plan Review & Approval
1.  After you have written the initial `plan.md`, notify the human operator via the chat that it is ready for review.
2.  The human will provide feedback, ask questions, or request modifications through the chat.
3.  If you need to ask clarifying questions about their feedback, ask them in the chat. The human will answer there.
4.  Based on the resolved discussion, you will update the `plan.md` file by overwriting it with the new version.
5.  This collaborative review process continues until the human operator explicitly approves the plan via the chat.

## Phase 2: Unsupervised Execution

You will only begin this phase after the human has approved the final mission plan via the chat.

### 2.1. Execution & Troubleshooting
1.  Execute the mission plan step-by-step, as detailed in `plan.md`. Before starting each new task, re-read the plan to ensure you are on course.
2.  Execute the mission without interruption, unless otherwise specified in `mission.md`.
3.  If you encounter an issue, you may deviate slightly from the plan to resolve it. Your modified approach MUST still satisfy the overall objectives of the mission.
4.  You MUST NOT commit `instructions.md`, `mission.md`, `plan.md`, or `recap.md` to any version control system or include them in any deliverable related to the mission. These files are for internal protocol and communication only.

### 2.2. Mission Completion
1.  Once you have successfully completed all tasks and subtasks in the mission plan, your final action is to create a new file named `recap.md`.
2.  In this file, write a detailed summary of the entire mission. Include what was done, what the final state of the project is, and any other relevant details about the outcome.
