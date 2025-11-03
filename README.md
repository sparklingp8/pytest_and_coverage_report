#  Python Test Coverage Demo

This project demonstrates how to use `pytest` and `coverage` to measure and report test coverage in a Python module.

---

## 📁 Project Structure

```
.
├── calculator.py         # Simple math functions
├── test_calculator.py    # Unit tests for calculator
├── .coveragerc           # Optional config to exclude test files
```

---

## ⚙️ Setup

Install required packages:

```bash
pip install pytest coverage
```

---

## Run Tests with Coverage

Run tests and track coverage:

```bash
coverage run -m pytest
```

Generate a coverage report:

```bash
coverage report
```

Optional: Generate an HTML report:

```bash
coverage html
```

Open `htmlcov/index.html` in a browser to view detailed coverage.

---

## Exclude Test Files from Coverage Report

Create a `.coveragerc` file to omit test files:

```ini
[run]
omit =
    test_*.py

[report]
exclude_lines =
    if __name__ == .__main__:
```

Then run:

```bash
coverage run -m pytest
coverage report
```

---

## Summary

- `pytest` runs your tests.
- `coverage` tracks which lines of your code are executed.
- You can exclude test files for cleaner, more meaningful reports.
