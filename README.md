# Day 9 — every file the notebooks touch

**You do not need to download anything.** Each notebook creates the files it needs in its
first cell, so it runs in a fresh Colab session with an empty folder. Verified: run from a
completely empty directory, the teaching notebook completes with no errors.

The four input files are copied here anyway, so you can open and read them without running
any code.

---

## Input files — provided here

These are the files the lessons *read*.

| File | Used by | Why it looks the way it does |
|---|---|---|
| `names.txt` | reading, `.strip()` | Three names. **The last line has no newline** — so `readlines()` gives `['Ravi\n', 'Sara\n', 'Amit']`. That asymmetry is what practice question A2 is about. |
| `marks.csv` | the whole CSV section | Four rows. Sara's city is `"Mumbai, MH"` — **a comma inside a quoted field**. On that row `split(",")` gives 5 fields while `csv.reader` gives 4. That single row is the entire argument for the csv module. |
| `cities.csv` | challenge D2 | A city-to-state lookup table. Also contains the quoted comma, so the merge only works if you read it properly. |
| `essay.txt` | challenge D1 | One sentence with repeated words, for the word-frequency exercise. `the` appears 4 times. |

---

## Output files — created when you run the notebooks

These are **produced by the lessons**. You do not need them in advance, and they will appear
in your working folder as you run the cells.

### Teaching notebook

| File | Created by |
|---|---|
| `demo.txt` | the `"w"` versus `"a"` demonstration — it gets deliberately overwritten to show that `"w"` destroys data |
| `out.txt`, `out2.txt`, `out3.txt` | the three ways of writing many lines (`write`, `writelines`, `print(file=f)`) |
| `simple.csv`, `dict.csv` | `csv.writer` and `csv.DictWriter` examples |
| `quoted.csv` | showing that the csv module adds quotes automatically |
| `report.csv` | the mini build's output |

### Practice notebooks

| File | Created by |
|---|---|
| `demo.txt` | questions A3 and A4 |
| `important.txt` | bug B1 — the file that gets destroyed by the wrong mode |
| `saved.txt`, `saved2.txt` | task C2 |
| `passed.csv` | task C3, the filtered rows |
| `app.log` | task C4, the append-only log |
| `averages.csv` | task C5 |
| `merged.csv` | challenge D2 |

---

## Files that are missing on purpose

| File | Why |
|---|---|
| `no_such_file.csv` | bug B4 — demonstrates `FileNotFoundError` and how to handle it |
| `does_not_exist.csv` | the same demonstration in the teaching notebook |

**Do not create these.** If they exist, the lesson they teach disappears.

---

## Working outside Colab

Put these four input files in the same folder as the notebook, or comment out the setup cell
so it does not overwrite them. Either works — the setup cell writes exactly the same content
that is in this folder.
