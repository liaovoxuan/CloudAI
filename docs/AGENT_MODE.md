# Agent Mode

Agent mode is designed for tasks that require more than a single response. It
can break a goal into steps, use the tools enabled by the user, update files,
run relevant checks and summarize the result.

## How it works

1. The user describes the goal and any constraints.
2. CloudAI inspects the available context and prepares the required steps.
3. It carries out authorized actions and reports meaningful progress.
4. It verifies the result where possible and provides a clear handoff.

Agent mode does not grant additional permissions by itself. It should request
confirmation before sensitive or destructive actions, and users should review
important changes before publishing or deploying them.

The application packages currently stored in the legacy archive are version
1.0.0 and do not represent the 1.0.1 Agent mode documentation.
