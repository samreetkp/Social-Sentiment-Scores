# Social Sentiment Analysis in Rust

This is a simple sentiment analysis program written in Rust. It reads a dictionary of social sentiment scores from a CSV file and evaluates the sentiment of a text review based on the individual word scores.

## Features

- Reads sentiment scores from `socialsent.csv` into a HashMap
- Accepts a review file (e.g., `review.txt`, `good.txt`, `bad.txt`) via command line
- Cleans and tokenizes words
- Accumulates sentiment scores and assigns a 1–5 star rating
- Implements modular design using three main subprograms:
  - `build_social_sentiment_table(...)`
  - `get_social_sentiment_score(...)`
  - `get_star_rating(...)`

 ## Files

- `main.rs` - main program file
- `socialsent.csv` - sentiment score dictionary file
- `review.txt`, `good.txt`, `bad.txt` - sample review files

## How to Run

### **Prerequisites**

Make sure you have:
- [Rust installed](https://www.rust-lang.org/tools/install) (includes `rustc` and `cargo`)
- The files:  
  - `main.rs` (your program)  
  - `socialsent.csv` (sentiment scores)  
  - At least one review file (e.g., `review.txt`, `good.txt`, `bad.txt`)

To check if Rust is installed, run:

```bash
rustc --version
```

---

### **Compile the Program**

In the terminal, compile the Rust file using:

```bash
rustc main.rs
```

This will generate an executable named `main` (or `main.exe` on Windows).

---
### **Run the Program**

You can run the program with:

```bash
./main review.txt
```

Or test it with another file:

```bash
./main good.txt
```

If no file name is provided, it will default to using `review.txt`:

```bash
./main
```

---

### Example Output

```
./main
[which: 0.00, 0.00]
[takes: 0.03, 0.03]
[multiple: -0.35, -0.32]
[delimeters: 0.00, -0.32]
[when: 0.00, -0.32]
[you: 0.00, -0.32]
[use: 0.10, -0.22]
[strtok: 0.00, -0.22]
[you: 0.00, -0.22]
[only: 0.00, -0.22]
[need: 0.02, -0.20]
[to: 0.00, -0.20]
[pass: 0.08, -0.12]
[it: 0.00, -0.12]
[the: 0.00, -0.12]
[address: -0.04, -0.16]
[of: 0.00, -0.16]
[your: 0.00, -0.16]
[buffer: 0.00, -0.16]
[the: 0.00, -0.16]
[first: 0.00, -0.16]
[time: 0.00, -0.16]
[after: 0.00, -0.16]
[that: 0.00, -0.16]
[just: 0.00, -0.16]
[pass: 0.08, -0.08]
[in: 0.00, -0.08]
[a: 0.00, -0.08]
[null: 0.00, -0.08]
[and: 0.00, -0.08]
[it: 0.00, -0.08]
[will: 0.00, -0.08]
[give: 0.13, 0.05]
[you: 0.00, 0.05]
[the: 0.00, 0.05]
[next: 0.17, 0.22]
[token: 0.00, 0.22]
[from: 0.00, 0.22]
[the: 0.00, 0.22]
[last: 0.52, 0.74]
[one: 0.00, 0.74]
[it: 0.00, 0.74]
[gave: -0.16, 0.58]
[you: 0.00, 0.58]
[returning: -0.11, 0.47]
[a: 0.00, 0.47]
[null: 0.00, 0.47]
[pointer: 0.00, 0.47]
[when: 0.00, 0.47]
[there: 0.00, 0.47]
[are: 0.00, 0.47]
[no: 0.00, 0.47]
[more: 0.00, 0.47]

review.txt Score: 0.47
review.txt Stars: ★★★
```
```
./main good.txt
[this: 0.00, 0.00]
[was: 0.00, 0.00]
[a: 0.00, 0.00]
[gift: 1.89, 1.89]
[for: 0.00, 1.89]
[my: 0.00, 1.89]
[grandson: 0.00, 1.89]
[he: 0.00, 1.89]
[used: -0.06, 1.83]
[these: -0.85, 0.98]
[product: 0.58, 1.56]
[during: -0.59, 0.97]
[his: 0.00, 0.97]
[internship: 0.00, 0.97]
[at: 0.00, 0.97]
[google: 0.00, 0.97]
[he: 0.00, 0.97]
[loves: -1.01, -0.04]
[it: 0.00, -0.04]
[and: 0.00, -0.04]
[says: 0.00, -0.04]
[it: 0.00, -0.04]
[works: 0.73, 0.69]
[perfect: 0.00, 0.69]
[product: 0.58, 1.27]
[as: 0.00, 1.27]
[stated: -0.66, 0.61]
[quick: 0.55, 1.16]
[delivery: 0.21, 1.37]
[this: 0.00, 1.37]
[is: 0.00, 1.37]
[an: 0.00, 1.37]
[amazing: 1.26, 2.63]
[setup: 0.00, 2.63]
[for: 0.00, 2.63]
[anybody: -0.04, 2.59]
[wanting: -0.02, 2.57]
[to: 0.00, 2.57]
[start: 0.29, 2.86]
[out: 0.00, 2.86]
[with: 0.00, 2.86]
[v60: 0.00, 2.86]
[all: 0.00, 2.86]
[pieces: 0.06, 2.92]
[arrived: 0.17, 3.09]
[in: 0.00, 3.09]
[perfect: 0.00, 3.09]
[condition: -0.63, 2.46]
[and: 0.00, 2.46]
[one: 0.00, 2.46]
[day: 0.49, 2.95]
[early: 0.85, 3.80]
[the: 0.00, 3.80]
[setup: 0.00, 3.80]
[is: 0.00, 3.80]
[compact: 1.03, 4.83]
[and: 0.00, 4.83]
[all: 0.00, 4.83]
[pieces: 0.06, 4.89]
[are: 0.00, 4.89]
[aesthetically: 0.00, 4.89]
[coordinated: 0.31, 5.20]
[it: 0.00, 5.20]
[looks: 0.04, 5.24]
[great: 1.48, 6.72]
[on: 0.00, 6.72]
[the: 0.00, 6.72]
[counter: -0.09, 6.63]
[the: 0.00, 6.63]
[set: 0.24, 6.87]
[is: 0.00, 6.87]
[thoughtfully: 0.00, 6.87]
[designed: 0.04, 6.91]
[too: -0.49, 6.42]
[the: 0.00, 6.42]
[stand: 0.01, 6.43]
[fits: 0.00, 6.43]
[perfectly: 2.69, 9.12]
[on: 0.00, 9.12]
[the: 0.00, 9.12]
[scale: 0.17, 9.29]
[the: 0.00, 9.29]
[bottom: 0.24, 9.53]
[of: 0.00, 9.53]
[the: 0.00, 9.53]
[stand: 0.01, 9.54]
[has: 0.00, 9.54]
[little: -0.54, 9.00]
[lips: 0.59, 9.59]
[that: 0.00, 9.59]
[hang: 0.12, 9.71]
[over: 0.00, 9.71]
[either: -0.19, 9.52]
[side: 0.14, 9.66]
[of: 0.00, 9.66]
[the: 0.00, 9.66]
[scale: 0.17, 9.83]
[to: 0.00, 9.83]
[keep: -0.01, 9.82]
[it: 0.00, 9.82]
[from: 0.00, 9.82]
[sliding: 0.09, 9.91]
[around: 0.70, 10.61]
[if: 0.00, 10.61]
[you: 0.00, 10.61]
[accidentally: 0.00, 10.61]
[knock: -0.32, 10.29]
[it: 0.00, 10.29]
[the: 0.00, 10.29]
[scale: 0.17, 10.46]
[itself: -0.28, 10.18]
[is: 0.00, 10.18]
[excellent: 0.00, 10.18]
[it: 0.00, 10.18]
[measures: 0.35, 10.53]
[to: 0.00, 10.53]
[the: 0.00, 10.53]
[tenth: 0.00, 10.53]
[of: 0.00, 10.53]
[a: 0.00, 10.53]
[gram: 0.00, 10.53]
[and: 0.00, 10.53]
[has: 0.00, 10.53]
[a: 0.00, 10.53]
[builtin: 0.00, 10.53]
[timer: 0.00, 10.53]
[which: 0.00, 10.53]
[is: 0.00, 10.53]
[extremely: -0.64, 9.89]
[useful: 0.84, 10.73]
[also: -0.01, 10.72]
[the: 0.00, 10.72]
[scale: 0.17, 10.89]
[does: 0.04, 10.93]
[not: 0.00, 10.93]
[shut: -0.58, 10.35]
[of: 0.00, 10.35]
[its: 0.00, 10.35]
[own: 0.93, 11.28]
[if: 0.00, 11.28]
[left: 0.52, 11.80]
[untouched: 0.34, 12.14]
[this: 0.00, 12.14]
[was: 0.00, 12.14]
[a: 0.00, 12.14]
[big: -1.22, 10.92]
[issue: -0.81, 10.11]
[with: 0.00, 10.11]
[the: 0.00, 10.11]
[kitchen: -0.69, 9.42]
[scale: 0.17, 9.59]
[i: 0.00, 9.59]
[used: -0.06, 9.53]
[to: 0.00, 9.53]
[employ: 0.00, 9.53]
[for: 0.00, 9.53]
[pourovers: 0.00, 9.53]
[very: 0.00, 9.53]
[frustrating: -1.46, 8.07]
[to: 0.00, 8.07]
[be: 0.00, 8.07]
[midpour: 0.00, 8.07]
[and: 0.00, 8.07]
[have: 0.00, 8.07]
[your: 0.00, 8.07]
[scale: 0.17, 8.24]
[shut: -0.58, 7.66]
[off: -0.17, 7.49]
[i: 0.00, 7.49]
[will: 0.00, 7.49]
[admit: -0.73, 6.76]
[that: 0.00, 6.76]
[the: 0.00, 6.76]
[price: 0.71, 7.47]
[for: 0.00, 7.47]
[the: 0.00, 7.47]
[whole: -1.40, 6.07]
[setup: 0.00, 6.07]
[is: 0.00, 6.07]
[a: 0.00, 6.07]
[bit: -0.72, 5.35]
[high: 0.02, 5.37]
[youre: 0.00, 5.37]
[mostly: -0.40, 4.97]
[paying: 0.27, 5.24]
[for: 0.00, 5.24]
[the: 0.00, 5.24]
[scale: 0.17, 5.41]
[which: 0.00, 5.41]
[goes: 0.07, 5.48]
[for: 0.00, 5.48]
[50: 0.00, 5.48]
[dollars: 0.24, 5.72]
[on: 0.00, 5.72]
[its: 0.00, 5.72]
[own: 0.93, 6.65]
[and: 0.00, 6.65]
[the: 0.00, 6.65]
[stand: 0.01, 6.66]
[which: 0.00, 6.66]
[goes: 0.07, 6.73]
[for: 0.00, 6.73]
[about: 0.00, 6.73]
[the: 0.00, 6.73]
[same: -0.34, 6.39]
[for: 0.00, 6.39]
[this: 0.00, 6.39]
[reason: -0.12, 6.27]
[id: 0.00, 6.27]
[only: 0.00, 6.27]
[recommend: 0.00, 6.27]
[this: 0.00, 6.27]
[product: 0.58, 6.85]
[if: 0.00, 6.85]
[youre: 0.00, 6.85]
[a: 0.00, 6.85]
[real: 0.29, 7.14]
[coffee: -0.65, 6.49]
[lover: 0.00, 6.49]
[with: 0.00, 6.49]
[a: 0.00, 6.49]
[good: 0.00, 6.49]
[grinder: 0.00, 6.49]
[good: 0.00, 6.49]
[beans: 0.08, 6.57]
[and: 0.00, 6.57]
[the: 0.00, 6.57]
[time: 0.00, 6.57]
[patience: 0.01, 6.58]
[to: 0.00, 6.58]
[fuss: 0.00, 6.58]
[around: 0.70, 7.28]
[with: 0.00, 7.28]
[pourover: 0.00, 7.28]
[technique: 0.30, 7.58]
[otherwise: -0.13, 7.45]
[for: 0.00, 7.45]
[a: 0.00, 7.45]
[beginner: 0.00, 7.45]
[an: 0.00, 7.45]
[aeropress: 0.00, 7.45]
[setup: 0.00, 7.45]
[is: 0.00, 7.45]
[simpler: 0.32, 7.77]
[less: -0.57, 7.20]
[fussy: 0.00, 7.20]
[and: 0.00, 7.20]
[less: -0.57, 6.63]
[expensive: -0.45, 6.18]
[and: 0.00, 6.18]
[will: 0.00, 6.18]
[still: 0.10, 6.28]
[give: 0.13, 6.41]
[you: 0.00, 6.41]
[great: 1.48, 7.89]
[cups: -0.02, 7.87]
[of: 0.00, 7.87]
[coffee: -0.65, 7.22]
[personally: -0.03, 7.19]
[im: 0.00, 7.19]
[thrilled: 0.00, 7.19]
[with: 0.00, 7.19]
[this: 0.00, 7.19]
[product: 0.58, 7.77]
[and: 0.00, 7.77]
[would: 0.00, 7.77]
[order: -0.02, 7.75]
[it: 0.00, 7.75]
[again: -0.43, 7.32]
[in: 0.00, 7.32]
[a: 0.00, 7.32]
[heartbeat: 0.00, 7.32]

good.txt Score: 7.32
good.txt Stars: ★★★★★
```
```
./main bad.txt
[so: 0.00, 0.00]
[ive: 0.00, 0.00]
[had: 0.00, 0.00]
[this: 0.00, 0.00]
[for: 0.00, 0.00]
[several: -0.43, -0.43]
[weeks: 0.21, -0.22]
[now: 0.00, -0.22]
[and: 0.00, -0.22]
[the: 0.00, -0.22]
[scale: 0.17, -0.05]
[is: 0.00, -0.05]
[already: -0.32, -0.37]
[on: 0.00, -0.37]
[the: 0.00, -0.37]
[fritz: 0.00, -0.37]
[its: 0.00, -0.37]
[not: 0.00, -0.37]
[working: 0.11, -0.26]
[at: 0.00, -0.26]
[all: 0.00, -0.26]
[and: 0.00, -0.26]
[its: 0.00, -0.26]
[basically: -0.64, -0.90]
[brand: 0.41, -0.49]
[new: -0.17, -0.66]
[buy: 0.11, -0.55]
[everything: 0.18, -0.37]
[but: 0.00, -0.37]
[the: 0.00, -0.37]
[scale: 0.17, -0.20]
[i: 0.00, -0.20]
[dont: 0.00, -0.20]
[know: 0.00, -0.20]
[how: 0.00, -0.20]
[to: 0.00, -0.20]
[return: 0.51, 0.31]
[it: 0.00, 0.31]
[unless: -0.05, 0.26]
[i: 0.00, 0.26]
[send: 0.21, 0.47]
[it: 0.00, 0.47]
[all: 0.00, 0.47]
[back: 0.00, 0.47]
[trimming: 0.00, 0.47]
[these: -0.85, -0.38]
[was: 0.00, -0.38]
[more: 0.00, -0.38]
[work: 0.40, 0.02]
[than: 0.00, 0.02]
[it: 0.00, 0.02]
[was: 0.00, 0.02]
[worth: 0.28, 0.30]
[ive: 0.00, 0.30]
[had: 0.00, 0.30]
[the: 0.00, 0.30]
[custom: 0.00, 0.30]
[orthotic: 0.00, 0.30]
[inserts: 0.00, 0.30]
[where: 0.00, 0.30]
[you: 0.00, 0.30]
[stand: 0.01, 0.31]
[on: 0.00, 0.31]
[the: 0.00, 0.31]
[machine: -0.13, 0.18]
[and: 0.00, 0.18]
[get: 0.00, 0.18]
[your: 0.00, 0.18]
[number: -0.03, 0.15]
[and: 0.00, 0.15]
[those: -0.38, -0.23]
[were: 0.00, -0.23]
[significantly: 0.33, 0.10]
[better: 0.06, 0.16]
[and: 0.00, 0.16]
[obviously: -0.21, -0.05]
[more: 0.00, -0.05]
[expensive: -0.45, -0.50]
[i: 0.00, -0.50]
[figured: -0.30, -0.80]
[since: 0.24, -0.56]
[these: -0.85, -1.41]
[are: 0.00, -1.41]
[made: -0.39, -1.80]
[by: 0.00, -1.80]
[the: 0.00, -1.80]
[same: -0.34, -2.14]
[people: 0.00, -2.14]
[they: 0.00, -2.14]
[should: 0.00, -2.14]
[be: 0.00, -2.14]
[equally: -0.27, -2.41]
[simple: 0.81, -1.60]
[and: 0.00, -1.60]
[comfortable: 2.22, 0.62]
[but: 0.00, 0.62]
[they: 0.00, 0.62]
[were: 0.00, 0.62]
[not: 0.00, 0.62]

bad.txt Score: 0.62
bad.txt Stars: ★★★
```
---
## Star Rating Scale

- Score < -5.0 → ⭐
- 5.0 ≤ Score < -1.0 → ⭐⭐
- 1.0 ≤ Score < 1.0 → ⭐⭐⭐
- 1.0 ≤ Score < 5.0 → ⭐⭐⭐⭐
- Score ≥ 5.0 → ⭐⭐⭐⭐⭐
