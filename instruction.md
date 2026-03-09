# Fix the Poker Probability Calculator

The script at `/app/poker_calculator.py` calculates poker hand probabilities but
the numbers are coming out wrong. It runs without crashing — the math is just off.

Fix it, then run:

```bash
python3 /app/poker_calculator.py
```

It should write `/app/poker_probabilities.json` with a `count` and
`probability_percent` for each of the 10 standard poker hands. All counts must
sum to **2,598,960** (total 5-card hands from a 52-card deck), and probabilities
must sum to **100.0**.
