---
name: arena
description: Coordinate multiple agents to solve complex problems through focused parallel work, independent analysis, and careful synthesis. Use when a task has separable parts, benefits from independent perspectives, or needs verification.
---

# Multi-Agent Problem Solving

## Goal

Use multiple agents to improve coverage and speed without sacrificing correctness. The lead agent owns the task, delegates bounded work, evaluates results, and delivers one coherent answer.

## Workflow

1. **Frame the problem**
   - Restate the goal, constraints, expected output, and what counts as success.
   - Identify uncertainties and risks.
   - Decide whether delegation will help. Keep the work with one agent if it is small, tightly coupled, or faster to solve directly.

2. **Decompose the work**
   - Split the task into independent, clearly scoped workstreams.
   - Give each agent a specific question or deliverable, relevant context, constraints, and expected format.
   - Avoid overlapping assignments unless independent verification is intentional.
   - Keep shared interfaces and assumptions explicit.

3. **Delegate in parallel**
   - Start independent workstreams concurrently when tools allow.
   - Ask agents to report their findings, evidence, assumptions, and unresolved questions.
   - Do not ask multiple agents to make conflicting changes to the same files or resources.
   - For implementation tasks, assign ownership of files or components and have one agent integrate.

4. **Track and unblock**
   - Monitor progress and resolve conflicting assumptions early.
   - If an agent is blocked, narrow the request, provide missing context, or reassign only the necessary work.
   - Do not delegate sensitive or consequential actions without clear authorization.

5. **Synthesize**
   - Compare findings rather than combining them mechanically.
   - Check claims against source material, tests, or other available evidence.
   - Resolve disagreements explicitly; do not treat majority opinion as proof.
   - Preserve useful caveats and distinguish verified facts from assumptions.

6. **Verify the result**
   - Check that the response or implementation satisfies the original goal and constraints.
   - Run appropriate tests or independent review when available.
   - Report failures, gaps, and remaining uncertainty honestly.

7. **Deliver**
   - Provide one clear, consistent result.
   - Summarize the approach and key decisions only as needed.
   - Credit or describe delegated work when useful, but avoid dumping raw agent transcripts.

## Delegation template

For each agent, provide:

- **Task:** One bounded question or deliverable.
- **Context:** Relevant background and constraints.
- **Scope:** What to cover and what not to cover.
- **Output:** Expected format, including evidence or file changes.
- **Coordination:** Dependencies, shared interfaces, and whether work must remain read-only.

## Fallback

If multiple agents or delegation tools are unavailable, simulate independent workstreams sequentially: analyze each perspective separately, then compare and verify the conclusions before answering.
