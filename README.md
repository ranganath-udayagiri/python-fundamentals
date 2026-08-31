# Python Fundamentals

Learning Python from the ground up by building a **support ticket triage tool** —
the same domain as a portfolio project I'm building later, so the practice
carries forward instead of being throwaway.

## Progress

| Day | Topic | Notebook |
|-----|-------|----------|
| 1–2 | Variables, data types, dictionaries | [day01-02](day01-02-variables-and-dicts.ipynb) |

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

## Approach

Predict → run → break → fix → explain back. Every exercise typed from scratch,
no copy-paste. The goal is mental models, not completed tutorials.
