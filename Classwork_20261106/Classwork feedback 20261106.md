# Classwork feedback 20261106

**Student:** Henry
**Classwork:** Classwork 20261106 — B2.2 Data structures
(arrays · pass-by-reference)
**Date:** 2026-11-06 · **Marked:** 2026-11-06
**Answer language:** written in A-Level pseudocode — accepted (full credit for correct content).

## Score

**84 / 100**

| Question | Score |
|---|---|
| Q1 — Reading arrays | 28/30 |
| Q2 — Writing array methods and a complete program | 17/30 |
| Q3 Part B — Pass-by-reference | 39/40 |

Full marked pages: `Classwork20261106_marked_p1..p3.png`

## Feedback on incorrect answers

**Q1(c) — 4/6**
- You identified the **runtime error** and the out-of-range index (0–4) — that is four of the six marks.
- The phrase **"fail to run" is not right**: a runtime error means the program **starts and then crashes** at that statement. Say that it stops/crashes there.

**Q2(b) — 7/20**
- Reading the eight values is correct, and your expected output (14.375 / 15 18 20 16) is correct.
- But the program never computes an average: it calls `countEven()` and then compares each temperature with `countEven()`. Call `average()` (or write the average calculation), store the result and compare with that. Not writing the average function itself is **not** penalised.

**Q3(d) — 9/10**
- The swap body and the output 9 5 are correct.
- The procedure header has **no name**. Write `PROCEDURE Swap(BYREF X : INTEGER, BYREF Y : INTEGER)`.

## What went well

- **Q1(a) and Q1(b) — full marks.** All five values and the complete trace table, with the correct output 8 21.
- **Q2(a) — 10/10.** A correct pseudocode function: array parameter, count initialised, loop over LENGTH, MOD test, RETURN.
- **Q3(a), Q3(b) and Q3(c) — full marks.** The trace, the BYREF explanation and the Replace procedure are all correct.

## Next steps

- When a question asks for an average, **call average (or write the calculation)** and use its result — do not reuse a different method.
- Say a runtime error **starts and then crashes**; "fails to run" describes a compile error.
- Write the procedure name in every header: `PROCEDURE Swap(...)`.
