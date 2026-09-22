# Python Fundamentals

Learning Python from the ground up by building a **support ticket triage tool** —
the same domain as a portfolio project I'm building later, so the practice
carries forward instead of being throwaway.

## Progress

| 1–9 | Variables, dicts, lists, conditionals, loops, functions, files/JSON, exceptions, classes | [day01-09](day01-09-python-fundamentals.ipynb) |

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

**Day 6 — Functions**
- `def` defines; nothing runs until the function is called
- Parameters are named slots filled at call time — use them, not globals
- `print` displays and is gone; `return` hands a value back to the caller
- No `return` → the function gives back `None`
- `return` exits immediately, so it goes after the loop, not inside it

**Day 7 — Files & JSON**
- `json.dumps`/`loads` work on strings; `json.dump`/`load` work on files
- `"w"` creates or wipes; `"r"` requires the file to exist
- `with` auto-closes the file
- Files persist across a restart; memory does not — the reason databases exist

**Day 8 — Exception handling**
- `try / except` catches by exception type, so error names matter
- Never use a bare `except:` — it swallows real bugs
- Return types should stay consistent across all paths

**Day 9 — Classes (OOP)**
- `class` is a blueprint, an object is one instance; `__init__` runs on creation
- `self` is this particular object; data is reached as `self.x` inside methods
- Methods are called without passing `self` — Python supplies it
- Methods can call each other through `self`
- A missing constructor argument raises `TypeError` at creation, so invalid objects can't exist
- Dicts for raw data in transit; classes for things with required fields and rules

## Approach

Predict → run → break → fix → explain back. Every exercise typed from scratch,
no copy-paste. The goal is mental models, not completed tutorials.
