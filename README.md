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


