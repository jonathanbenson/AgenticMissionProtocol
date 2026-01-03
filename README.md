# Agentic Mission Protocol

## Overview

This repository contains a detailed instruction set (`instructions.md`) designed to guide an agentic AI through a structured, two-phase mission. The protocol ensures robust planning, clear communication, and autonomous execution, making it ideal for complex tasks managed via a command-line interface (CLI).

The core philosophy is to spend significant time in a **Collaborative Planning** phase with a human operator to create a detailed, atomic plan. Once the human approves the plan, the agent enters an **Unsupervised Execution** phase where it has the autonomy to complete the mission without further intervention.

## How It Works

The process is governed by the `instructions.md` file and relies on a set of markdown files for communication between the human and the AI agent.

### Phase 1: Collaborative Planning

1.  **Mission Briefing & Research**: The agent starts by reading a `mission.md` file that you, the human operator, create. It then uses its tools to conduct preliminary research to ensure it understands the mission's context and requirements.
2.  **Q&A**: The agent asks clarifying questions about the mission in a `discourse.md` file. You provide answers in the same file. This cycle continues until the agent has all the information it needs.
3.  **Plan Development**: The agent creates a detailed `plan.md`, breaking the mission down into atomic tasks and subtasks.
4.  **Plan Review**: You review the `plan.md`. Any feedback or required changes are discussed in the `discourse.md` file. The agent updates the plan until you give final approval.

### Phase 2: Unsupervised Execution

1.  **Execution**: The agent autonomously executes the approved `plan.md` step-by-step.
2.  **Problem-Solving**: If an issue occurs, the agent has the autonomy to try and resolve it by deviating from the specific planned step, as long as the solution still meets the mission's goals.
3.  **Protocol Discipline**: The agent is instructed NEVER to commit protocol-specific files (`instructions.md`, `mission.md`, `discourse.md`, `plan.md`, or `recap.md`) to version control.
4.  **Recap**: Upon successful completion of all tasks, the agent will generate a `recap.md` file summarizing everything that was done.

## How to Use

1.  **Define Your Mission**: Create a `mission.md` file in your project directory. Clearly define the goals, requirements, constraints, and any other relevant information for the agent.
2.  **Provide the Protocol**: When you start your agentic AI CLI, provide the contents of `instructions.md` as its initial system prompt or first instruction. This tells the agent to follow the mission protocol.
3.  **Collaborate**:
    - Look for the agent to create a `discourse.md` file with questions. Answer them.
    - Review the `plan.md` file when the agent creates it.
    - Provide feedback in `discourse.md` until the plan is perfect.
    - Approve the plan by stating so in `discourse.md`.
4.  **Observe**: Once you approve the plan, the agent will begin execution. You can monitor its progress, but no further interaction is needed unless it reports a mission failure.
5.  **Review**: Once the mission is complete, read the `recap.md` for a full summary of the work performed.

## File Reference

-   `instructions.md`: The master instruction set for the AI agent.
-   `mission.md`: **(Human-created)** Details the mission objectives.
-   `discourse.md`: **(Agent-created)** Used for Q&A and feedback between human and agent.
-   `plan.md`: **(Agent-created)** The detailed, step-by-step mission plan.
-   `recap.md`: **(Agent-created)** The final summary of the completed mission.
