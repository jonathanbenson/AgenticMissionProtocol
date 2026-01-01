# Mission Protocol

Your mission is divided into two distinct phases: Phase 1 for collaborative planning and Phase 2 for unsupervised execution. You must adhere to this protocol strictly.

## Phase 1: Collaborative Planning

This phase is iterative and requires collaboration with the human operator to ensure the plan is robust and meets all requirements.

### 1.1. Mission Briefing & Research
1.  Read the `mission.md` file to understand the primary objectives, constraints, and requirements of your mission.
2.  Utilize your available tools to conduct preliminary research. This is to ensure you are familiar with the concepts, technologies, and context of the mission.

### 1.2. Initial Questions & Clarification
1.  After your initial review and research, you must formulate questions to resolve any ambiguities or to gather more details.
2.  Create a new file named `discourse.md`.
3.  Write your questions in this file. Format them clearly, leaving space for the human operator to write answers directly next to or below each question.
4.  Await the human's response in `discourse.md`.
5.  Once the human has answered, review their responses. If you have follow-up questions, you will override the `discourse.md` file with the new set of questions.
6.  This question-answer cycle continues until you have no further questions and all mission parameters are clear to you.

### 1.3. Plan Development
1.  Once all your initial questions are answered, create a new file named `plan.md`.
2.  Develop a comprehensive mission plan. This plan must be broken down into a hierarchical structure of tasks and subtasks.
3.  **Subtasks must be atomic operations.** An atomic operation is a single, indivisible action (e.g., create a file, write content to a file, run a specific command, call a single tool).
4.  The plan must be detailed enough that every single action you will take is explicitly listed in the correct sequence.

### 1.4. Plan Review & Approval
1.  After you have written the initial `plan.md`, the human operator will review it.
2.  The human will provide feedback, ask questions, or request modifications by writing in the `discourse.md` file.
3.  You will review their feedback. If you need to ask clarifying questions about their feedback, write your follow-up questions in `discourse.md`. The human will answer them there.
4.  Based on the resolved discussion, you will update the `plan.md` file by overwriting it with the new version.
5.  This collaborative review process continues until the human operator explicitly approves the plan.

## Phase 2: Unsupervised Execution

You will only begin this phase after the human has approved the final mission plan.

### 2.1. Execution
1.  Execute the mission plan step-by-step, exactly as detailed in `plan.md`.
2.  Before starting each new task, you must re-read the `plan.md` file to ensure you are still on course.
3.  You must not deviate from the approved plan. Do not pause for human input or confirmation during execution unless an unforeseen issue forces a plan change.
4.  You MUST NOT commit `instructions.md`, `mission.md`, `discourse.md`, `plan.md`, or `recap.md` to any version control system or include them in any deliverable related to the mission. These files are for internal protocol and communication only.

### 2.2. Handling Contingencies
1.  If you encounter an unforeseen technical issue (e.g., a command fails unexpectedly, a library is incompatible, an API returns an error) that makes the current plan impossible to follow, you must pause execution.
2.  You will then formulate a new, updated plan to address the issue.
3.  This new plan must be written to `plan.md`, and it must undergo the same rigorous review and approval process as defined in **Section 1.4**, using the `discourse.md` file for communication.
4.  Do not resume execution until the human has approved the revised plan.

### 2.3. Mission Completion
1.  Once you have successfully completed all tasks and subtasks in the mission plan, your final action is to create a new file named `recap.md`.
2.  In this file, write a detailed summary of the entire mission. Include what was done, what the final state of the project is, and any other relevant details about the outcome.
