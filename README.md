# Integer Overflow Lab

An interactive, browser-based teaching module for understanding **integer/arithmetic overflow**.

## What it demonstrates

The app lets learners:

- choose a fixed integer width (4, 8, or 16 bits);
- choose addition or multiplication and enter two values;
- click **Calculate** to apply the selected scenario; and
- see the mathematical result;
- see the value that is actually stored after modulo wrapping;
- compare unsigned and signed two's-complement interpretations;
- inspect the individual bits;
- answer a rotating set of six knowledge-check questions; and
- track a quiz score and start a new shuffled quiz.

For example, with an 8-bit signed integer, `127 + 1` produces the bit pattern `10000000`. That pattern is `128` when interpreted as unsigned, but `-128` when interpreted as signed two's complement.

## Files

- `index.html` — the complete self-contained interactive application.
- `README.md` — project documentation.
- `reflection.md` — reflection on the AI-assisted development workflow and learning.

## How to run

No build system or dependencies are required.

1. Download or clone the repository.
2. Open `index.html` in a standard web browser.
3. Change the width and inputs and notice the changes.
4. Use the quick-check section to test your understanding.

A simple local server also works:

```bash
python3 -m http.server
```

Then open the local address shown by Python.

## Learning goal

The goal is to make fixed-width arithmetic concrete. A mathematical integer can grow without this restriction, but a machine integer has a limited number of bits. When the result cannot be represented, the stored bit pattern can wrap around. The same bits can also have different numerical meanings depending on whether the program interprets them as signed or unsigned.

This module intentionally stays on the educational side of the topic. It does not provide exploit code, shellcode, or an attack workflow.

## AI-assisted development

AI was used to help plan the interaction, draft the HTML/CSS/JavaScript structure, and create the project documentation. The generated code was reviewed and organized into a single static file so the project remains easy to inspect and run.
