# Classwork feedback 20261009

**Student:** Henry
**Classwork:** Classwork 20261009 — B2.3 Programming Constructs
(functions · selection · repetition · library functions incl. `Random`)
**Date:** 2026-10-09 · **Marked:** 2026-10-09
**Answer language:** written in Java — accepted (A-Level pseudocode was also allowed).

## Score

**83 / 100**

| Question | Score |
|---|---|
| Q1 — Reading functions and loops | 30/30 |
| Q2 — Library functions: the `Random` class | 23/30 |
| Q3 — Writing a complete program (Collatz) | 30/40 |

Full marked pages: `Classwork20261009_marked_AS_20261009_Henry_p1..p3.png`

## Feedback on incorrect answers

**Q2 (a) (iii) — 1/2**
- "The loop repeats four times" is right. The second mark is for saying that `nextInt()` produces
  a **new** value on each call — that is what makes four *different* numbers appear.

**Q2 (a) (iv) — 1/4**
- "More readable and maintainable" is the advantage from **slide 35 (modularisation)**, not the
  library-functions slide. **Slide 38** gives exactly two:
  - **Reuse of code** — essential functions are common to many programs, so they do not have to be
    written again.
  - **Improve reliability** — library code is thoroughly tested, so it can be relied on.
- You also need to link each one back to this program: `rnd.nextInt(6)` is called instead of the
  programmer writing (and testing) their own random-number generator.

**Q2 (c) (i) — 2/3**
- The range **and** the fact that 1.0 is excluded are both there — good.
- Add the shape's detail: a circle of **radius 0.5 centred at (0.5, 0.5)**. The 0.25 in the test is
  r², not the radius.

**Q2 (c) (iii) — 1/3**
- Your answer says a `double` is needed for the result, which is only half the story. The real
  reason is **integer division**: `cnt` and `N` are both `int`, so `4 * cnt / N` is evaluated in
  whole numbers and the fractional part is thrown away. Writing `4.0` forces the whole expression
  to use `double` arithmetic.

**Q3 (b) — 7/10**
- The loop structure is right and the count is right, but two things break the function:
  1. `num` is **never given the value of the parameter `n`** — it is declared and then used
     uninitialised. It needs `num <- n` before the loop.
  2. The `INPUT num` **inside** the loop makes the function read from the keyboard on every pass
     instead of working through the sequence. Delete it — the value comes in as a parameter.

**Q3 (d) — 9/16**
- Your sequence output stops at **2**: the `WHILE NOT (n = 1)` loop exits as soon as `n` becomes 1,
  so the final `1` is never printed. Either print it once more after `ENDWHILE`, or use a
  `REPEAT … UNTIL` loop so the body always runs at least once.
- `steps(n)` is called **after** the loop has turned `n` into 1, so it would print `Steps: 0`.
  Keep the number the user typed in a second variable and pass that instead.
- Your two expected outputs (8 and 16) are both correct — the code just does not produce them yet.

## What went well

- **Q1 — full marks (30/30).** Part (d) is a model answer: both the void case (`countUp`) and the
  value case (`area`, `label`) are explained *with examples from this question*, exactly as asked.
- **Q2 (c) (ii) is a perfect answer.** Writing `A_circle = πr² = 0.25π`, `A_square = 1`, then
  `0.25π / 1 = cnt / N` and `π = 4 × cnt / N` is precisely the reasoning the mark scheme wants.
- **Q2 (b) (i) and (ii)** — clean, correct, and `main` calls `roll()` exactly five times.
- **Q3 (a)** — correct, and using `n / 2` (integer division on an `int`) is the right call.
- **Q3 (c)** — a complete answer: unknown repetition count, and a condition-controlled loop rather
  than a counter-controlled one.

## Next steps

1. **Quote the slide.** When a question names a slide ("Slide 38 gives advantages of …"), the marks
   come from that slide's own wording. Read the bullet points back at the examiner.
2. **Trace the parameter into the function body.** In Q3 (b) ask, for every variable you declare:
   *where does its first value come from?* `num` had no answer to that question. Similarly, a
   function must never read input for a value it was already given as a parameter.
3. **Test the edges.** Q3 (d) is designed around two traps: the final term, and keeping the
   original input. Run 6 through your own code against your expected output before handing in —
   the two would not have matched.
