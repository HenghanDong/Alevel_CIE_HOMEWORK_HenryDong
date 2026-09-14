# Classwork feedback 20260911

**Student:** Henry
**Classwork:** Classwork 01 — B2.1 Programming Fundamentals (variables, data types, substring manipulation)
**Date:** 2026-09-11
**Marked:** 2026-09-14

## Score

**75 / 100**

| Question | Score |
|---|---|
| Q1 — data types, naming, print vs println | 12/12 |
| Q2 — string manipulation (tracing) | 10/14 |
| Q3 — scope of variables + tracing | 12/16 |
| Q4 — debugging and scope | 11/14 |
| Q5 — program using all data types | 16/20 |
| Q6 — substring-manipulation program | 14/24 |

Note: `Classwork01_20260911_marked_p1.png` … `_p3.png` in this folder show every
mark and deduction in place on your script.

## Feedback on incorrect answers

**Q2 (d) (-2 marks)**
- You wrote `Information T`. `s.substring(12)` gives the characters from index
  12 **to the end of the string**, so the output is `Technology` — the whole
  word, not just its first letter.

**Q2 (f) (-2 marks)**
- You wrote `error, string "xyz" doesn't exist`. `indexOf` does **not** raise an
  error when the substring is absent — it returns **-1**. The printed output is
  `-1`.

**Q3 (a) (-2 marks)**
- Your revised three-row table has every value correct
  (`x = 8` throughout, `y (global) = 2` throughout, `y (local) = 10` then `13`,
  and all three output lines correct) — a strong answer.
- The only loss is that the table starts *after* `update()` has already run, so
  the **initial state** (`x = 5`, `y = 2`, no local variable, no output) is not
  shown. The question asks for the value at **every step**.

**Q4 (a) (-3 marks)**
- "`score` isn't defined in `increaseScore()`. It is a new local variable, so
  `score + 10` doesn't make sense" — the middle clause is the important one and
  it is right. Name the mechanism to secure the marks: the declaration is
  **self-referential** — the `score` on the right-hand side refers to the new
  local variable, which is **not yet initialised**. Hence *"variable score might
  not have been initialized"*.

**Q5 (-4 marks)**
- You answered in **A-Level pseudocode** (`DECLARE … : INTEGER`, `←`, `OUTPUT(…)`).
  As an A-Level student this is accepted, and the substance is right:
  - All five data types are declared, with good camelCase names — full marks.
  - The concatenation has one bug: `"studentScore"` in quotes prints the **word**,
    not the value. Write `studentScore` without quotes to join the value.
- You output only two of the five values, and no expected output is shown.

**Q6 (-10 marks)**
- Also answered in **A-Level pseudocode** (`MID`, `UCASE`) — accepted for A-Level.
  Your extraction positions are right: `MID(fullName, 2, 16)` gives the trimmed
  name, `2 … 8` gives `Michael`, `10 … 16` gives `Jackson`, and `UCASE` gives the
  upper case — so (a)–(d) earn nearly full credit.
- Two things to tighten:
  - State the index convention you are using. Your numbers work if the end
    position is **inclusive**; with Java's own convention (`substring(start, end)`,
    end **exclusive**) the same numbers would give `Michae` and `Jackso`.
  - (e) and (f) were not attempted: the e-mail domain (`indexOf("@") + 1`) and
    `replace("mjackson", "mj")`.

## What went well

- **Q1 was perfect (12/12)** — the only student to score full marks on it. All
  four judgements in (b) carry reasons, and (c) is fully correct.
- Q3 (b): a clean, correct explanation of local vs global.
- Q4 (b): the fix is right **and** you stated the output `Final score: 10` —
  the only student to do both.
- Q6: getting `2…8` for `Michael` and `10…16` for `Jackson` shows you can work
  out substring boundaries from a raw string, leading spaces and all.

## Next steps

1. `indexOf` returns an **int index**, and **-1** when not found.
2. `substring(n)` without an end index takes everything to the end of the string.
3. Remember the initial state in a trace table (`x = 5` before `update()` runs).
4. In pseudocode, `"studentScore"` is a **string literal** — drop the quotes to
   output the variable's value.
5. Always state which index convention you are using when you write `MID`.

---
_Marks and margin notes are also marked up on your scanned script
(`Classwork01_20260911_marked_p1.png` … `_p3.png`)._
