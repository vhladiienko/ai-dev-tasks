# 🎮 AI Game Dev Tasks for Cursor 🤖

Welcome to **AI Game Dev Tasks**! This repository provides a collection of `.mdc` (Markdown Command) files designed to supercharge your game development workflow within the [Cursor](https://cursor.sh/) editor. By leveraging these commands with Cursor's AI Agent, you can systematically approach building game features and systems, from ideation to implementation, with built-in checkpoints for verification.

Stop wrestling with monolithic AI requests and start guiding your AI collaborator step-by-step through game development!

## ✨ The Core Idea

Building complex game features with AI can sometimes feel like a black box. This workflow aims to bring structure, clarity, and control to the process by:

1.  **Defining Scope:** Clearly outlining what needs to be built with a Game Design Document (GDD).
2.  **Detailed Planning:** Breaking down the GDD into a granular, actionable task list.
3.  **Iterative Implementation:** Guiding the AI to tackle one task at a time, allowing you to review and approve each change.

This structured approach helps ensure the AI stays on track, makes it easier to debug issues, and gives you confidence in the generated code and game systems.

## Workflow: From Game Idea to Implemented Feature 💡➡️🎮

Here's the step-by-step process using the `.mdc` files in this repository:

### 1️⃣ Create a Game Design Document (GDD)

First, lay out the blueprint for your game feature or system. A GDD clarifies what you're building, how players will interact with it, and why it's fun.

You can create a lightweight GDD directly within Cursor:

1.  Ensure you have the `create-gdd.mdc` file from this repository accessible.
2.  In Cursor's Agent chat, initiate GDD creation:

    ```
    Use @create-gdd.mdc
    Here's the game feature I want to build: [Describe your feature/mechanic in detail]
    Reference these files to help you: [Optional: @GameManager.cs @PlayerController.cs]
    ```
    *(Pro Tip: For complex GDDs, using MAX mode in Cursor is highly recommended if your budget allows for more comprehensive generation.)*

### 2️⃣ Generate Your Task List from the GDD

With your GDD drafted (e.g., `gdd-upgrade-system.md`), the next step is to generate a detailed, step-by-step implementation plan for your AI Developer.

1.  Ensure you have `generate-tasks.mdc` accessible.
2.  In Cursor's Agent chat, use the GDD to create tasks:

    ```
    Now take @gdd-upgrade-system.md and create tasks using @generate-tasks.mdc
    ```
    *(Note: Replace `@gdd-upgrade-system.md` with the actual filename of the GDD you generated in step 1.)*

### 3️⃣ Examine Your Task List

You'll now have a well-structured task list, often with tasks and sub-tasks, ready for the AI to start working on. This provides a clear roadmap for implementation, including code files, game assets, and testing protocols.

### 4️⃣ Instruct the AI to Work Through Tasks (and Mark Completion)

To ensure methodical progress and allow for verification, we'll use `process-task-list.mdc`. This command instructs the AI to focus on one task at a time and wait for your go-ahead before moving to the next.

1.  Create or ensure you have the `process-task-list.mdc` file accessible.
2.  In Cursor's Agent chat, tell the AI to start with the first task (e.g., `1.1`):

    ```
    Please start on task 1.1 and use @process-task-list.mdc
    ```
    *(Important: You only need to reference `@process-task-list.mdc` for the *first* task. The instructions within it guide the AI for subsequent tasks.)*

    The AI will attempt the task and then prompt you to review.

### 5️⃣ Review, Approve, and Progress ✅

As the AI completes each task, you review the changes.
*   If the changes are good, simply reply with "yes" (or a similar affirmative) to instruct the AI to mark the task complete and move to the next one.
*   If changes are needed, provide feedback to the AI to correct the current task before moving on.

You'll see a satisfying list of completed items grow, providing a clear visual of your game feature coming to life!

While it's not always perfect, this method has proven to be a very reliable way to build out larger game features and systems with AI assistance.

## 🗂️ Files in this Repository

*   **`create-gdd.mdc`**: Guides the AI in generating a Game Design Document for your feature, focusing on player experience, game mechanics, and core gameplay loops.
*   **`generate-tasks.mdc`**: Takes a GDD markdown file as input and helps the AI break it down into a detailed, step-by-step implementation task list covering code, assets, and testing.
*   **`process-task-list.mdc`**: Instructs the AI on how to process the generated task list, tackling one task at a time and waiting for your approval before proceeding. (This file also contains logic for the AI to mark tasks as complete).

## 🌟 Benefits

*   **Structured Game Development:** Enforces a clear process from game idea to playable feature.
*   **Step-by-Step Verification:** Allows you to review and approve AI-generated code and assets at each small step, ensuring quality and control.
*   **Manages Complexity:** Breaks down large game systems into smaller, digestible tasks for the AI, reducing the chance of it getting lost or generating overly complex, incorrect implementations.
*   **Improved Reliability:** Offers a more dependable approach to leveraging AI for significant game development work compared to single, large prompts.
*   **Clear Progress Tracking:** Provides a visual representation of completed tasks, making it easy to see how much has been done and what's next.
*   **Game Engine Agnostic:** While examples show Unity-specific files, the workflow adapts to any game engine or framework.
*   **Perfect for Game Jams:** Rapid prototyping workflow ideal for time-constrained development.

## 🛠️ How to Use

1.  **Clone or Download:** Get these `.mdc` files into your project or a central location where Cursor can access them.
2.  **Follow the Workflow:** Systematically use the `.mdc` files in Cursor's Agent chat as described in the 5-step workflow above.
3.  **Adapt and Iterate:**
    *   Feel free to modify the prompts within the `.mdc` files to better suit your specific game engine, genre, or development style.
    *   If the AI struggles with a task, try rephrasing your initial feature description or breaking down tasks even further.

## 💡 Tips for Success

*   **Be Specific About Player Experience:** The more context you provide about how the feature should *feel* to play, the better the AI's output will be.
*   **MAX Mode for GDDs:** As mentioned, using MAX mode in Cursor for GDD creation (`create-gdd.mdc`) can yield more thorough and higher-quality results if your budget supports it.
*   **Correct File Tagging:** Always ensure you're accurately tagging the GDD filename (e.g., `@gdd-upgrade-system.md`) when generating tasks.
*   **Think in Systems:** Game features rarely exist in isolation. Consider how your feature integrates with existing game systems.
*   **Balance and Polish:** Don't forget to include balance considerations and juice/polish requirements in your GDDs.
*   **Playtesting:** Remember that the best game design documents lead to features that need playtesting and iteration.

## 🎯 Perfect For

*   **Solo Indie Developers:** Streamline your development process and maintain focus on player experience.
*   **Game Jam Participants:** Rapidly prototype and implement game mechanics under tight deadlines.
*   **Learning Game Development:** Understand how to break down complex game systems into manageable pieces.
*   **Any Game Genre:** From idle clickers to RPGs, the workflow adapts to your game's needs.

## 🤝 Contributing

Got ideas to improve these `.mdc` files or have new ones that fit this game development workflow? Contributions are welcome!
Please feel free to:
*   Open an issue to discuss changes or suggest new features.
*   Submit a pull request with your enhancements.
*   Share your success stories using this workflow!

---

Happy AI-assisted game developing! 🎮✨
