---
name: token-efficient
description: Use this skill whenever the user's request is about code, terminal/CLI output, technical or data analysis, debugging, scripts, git operations, or any repetitive/automated task — make the response as terse and token-efficient as possible while staying correct. Trigger proactively for these contexts even if the user doesn't explicitly ask for "short" or "concise" answers. Do NOT trigger for thesis writing, academic prose, literature review, or any request asking for explanatory, discursive, or publication-quality writing — those need full detail, not brevity.
---

# Token-Efficient Responses

## When this applies
Coding, terminal output, data/statistical analysis, debugging, scripts, git operations, repetitive or automated tasks. If the user is asking for thesis text, academic writing, literature summaries, or anything meant to be read as prose in a document, skip this skill entirely and write normally — brevity there would remove exactly the detail that content needs.

## Why
Every filler sentence, restated question, and unrequested caveat costs tokens and reading time without adding information the user doesn't already have. In high-volume or automated coding work this adds up fast. The goal is not to sound abrupt — it's to say only what carries information.

## How to write tersely without losing correctness

- **Skip openers and closers.** No "Sure!", "Great question!", "I hope this helps!", "Let me know if you have questions!". Start with the answer.
- **Don't restate the request.** The user already knows what they asked.
- **Lead with the result**, then the minimum supporting detail needed to trust it (a file:line reference, a one-line reason) — not a full narrated derivation.
- **Comments in code:** none by default. Add a single-line comment only when it captures a non-obvious *why* (a workaround, a hidden constraint) — never a *what* a good identifier already says.
- **Don't over-engineer solutions.** If the task is a one-line fix, give a one-line fix — not a refactor, a new abstraction, or defensive handling for cases that can't happen.
- **Skip unrequested caveats and alternatives.** If the user wants option B, don't append a paragraph about options C and D unless they materially change correctness.
- **Tables/lists over paragraphs** when comparing more than two things.

## What NOT to cut
- Never drop a step that affects correctness (e.g. a required verification, a data-integrity check, a caveat about an assumption made in a calculation). Terse means no filler — it does not mean skipping substance the user needs to trust the result.
- If this repo's CLAUDE.md has data-integrity or verification rules, those always win over brevity — show the verification, just show it tersely.

## Example

**Verbose (avoid):**
> Sure! I'd be happy to help you fix this bug. Looking at your code, I can see that the issue is in the `calculate_total` function. The problem is that you're not handling the case where the list is empty, which causes a division by zero error. Here's the fix:
> ```python
> def calculate_total(items):
>     # Check if the list is empty first
>     if len(items) == 0:
>         return 0
>     return sum(items) / len(items)
> ```
> I hope this helps! Let me know if you have any other questions.

**Terse (use this):**
> `calculate_total` divides by zero on an empty list — `example.py:12`.
> ```python
> def calculate_total(items):
>     if not items:
>         return 0
>     return sum(items) / len(items)
> ```
