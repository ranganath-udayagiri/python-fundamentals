# Python Fundamentals

Learning Python from the ground up by building a **support ticket triage tool** —
the same domain as a portfolio project I'm building later, so the practice
carries forward instead of being throwaway.

## Progress

| Day | Topic | Notebook |
|-----|-------|----------|
| 1–5 | Variables, dicts, lists, conditionals, loops | [day01-05](day01-05-python-fundamentals.ipynb) |

## Concepts covered

**Day 1 — Variables & types**
- `int` / `str` / `bool` / `float`, and why Python won't guess between them
- `TypeError` on `"text" + 101` — `+` means addition for numbers, concatenation for strings
- f-strings as the readable fix

**Day 2 — Dictionaries**
- Key/value records: one ticket = one dict, instead of loose variables per field
- `KeyError` vs `TypeError` — missing key vs wrong type
- `ticket["x"]` demands a field and crashes if absent; `ticket.get("x", default)` asks and degrades gracefully
- Keys are a contract: `status` and `priority` are different questions and need different keys

**Day 3 — Lists**
- Ordered collections, zero-based indexing, `IndexError`
- `[-1]` for the last item; `.append()` to add
- **List of dictionaries** — the shape every API, DB query and RAG retrieval returns
- Mutation vs assignment: `.append()` accumulates on re-run, `=` overwrites

**Day 4 — Conditionals**
- `if / elif / else`; `=` assigns, `==` compares
- Indentation is syntax, not style — `IndentationError`
- `elif` stops at the first match, so order the specific conditions first

**Day 5 — Loops**
- `for` over a list; combined with `if` to build a working triage tool
- Counting into a variable and filtering into a list — same four-step pattern
- `while` for unknown-length loops (retries, agent loops); infinite-loop failure mode
- `break` for early exit

## Approach

Predict → run → break → fix → explain back. Every exercise typed from scratch,
no copy-paste. The goal is mental models, not completed tutorials.
