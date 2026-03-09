# Poker Probability Theory Calculator

A Python-based calculator for computing poker hand probabilities using combinatorial mathematics.

## Overview

This project calculates the probability of all 10 standard poker hands from a 52-card deck. The calculator determines both the count of each hand type and their probability percentages.

## Features

- **Complete Hand Analysis**: Calculates probabilities for all 10 poker hands
- **Mathematical Accuracy**: Uses proper combinatorial formulas
- **Validation**: Ensures total hand count equals 2,598,960 (C(52,5))
- **Docker Support**: Containerized environment for consistent execution
- **Automated Testing**: Comprehensive test suite to verify calculations

## Poker Hands Calculated

1. **Royal Flush** - A, K, Q, J, 10 of the same suit
2. **Straight Flush** - Five cards in sequence, same suit
3. **Four of a Kind** - Four cards of the same rank
4. **Full House** - Three of a kind + a pair
5. **Flush** - Five cards of the same suit
6. **Straight** - Five cards in sequence
7. **Three of a Kind** - Three cards of the same rank
8. **Two Pair** - Two pairs of different ranks
9. **One Pair** - Two cards of the same rank
10. **High Card** - None of the above

## Requirements

- Python 3.12
- Docker (for containerized execution)

## Installation

### Using Docker (Recommended)

```bash
cd environment
docker build -t poker-calculator .
docker run -v $(pwd)/..:/app poker-calculator
```

### Local Installation

```bash
pip install -r requirements.txt  # if requirements.txt exists
```

## Usage

### Running the Calculator

```bash
python3 poker_calculator.py
```

This will generate `poker_probabilities.json` with the results.

### Expected Output

The output file contains probability data for each hand type:

```json
{
  "royal_flush": {
    "count": 4,
    "probability_percent": 0.000154
  },
  "straight_flush": {
    "count": 36,
    "probability_percent": 0.00139
  },
  // ... other hands
}
```

**Validation Requirements:**
- Sum of all counts = 2,598,960
- Sum of all probabilities = 100.0%

## Testing

Run the test suite to verify calculations:

```bash
./tests/test.sh
```

Or run individual tests:

```bash
python3 tests/test_outputs.py
```

## Project Structure

```
poker-probability-theory/
├── environment/
│   ├── Dockerfile
│   └── poker_calculator.py    # Main calculator script
├── solution/
│   └── solve.sh              # Solution runner
├── tests/
│   ├── test.sh               # Test runner
│   └── test_outputs.py       # Output validation
├── instruction.md            # Problem description
├── task.toml                 # Project configuration
├── .gitignore               # Git ignore rules
└── README.md                # This file
```

## Mathematical Foundation

The calculations use combinatorial mathematics:

- **Total hands**: C(52, 5) = 2,598,960
- **Hand probabilities**: (favorable outcomes) / (total outcomes) × 100%

Where C(n, k) represents combinations of n items taken k at a time.

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Run tests to ensure accuracy
5. Submit a pull request

## License

This project is for educational purposes. Please refer to the task configuration for usage rights.

## Author

**Jordan Mitchell**  
jordan.mitchell@devmail.io

*Difficulty: Easy | Category: SWE | Tags: Python, Mathematics, Debugging, Combinatorics, Poker*