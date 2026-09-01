# Module Lab: Automating Python Projects with Pip, PyPi & Scripting

This project contains two small automation scripts built for this lab.

## Files

- **`generate_log.py`** — Writes a list of log entries to a timestamped
  `.txt` file (`log_YYYYMMDD.txt`). Includes input validation (raises
  `ValueError` for non-list input) and prints a confirmation message.

- **`fetch_data.py`** — Uses the `requests` package to fetch data from a
  public API (JSONPlaceholder), then writes the result to a timestamped
  `.txt` file. Demonstrates using a pip-installed third-party package
  and File I/O together.

- **`requirements.txt`** — Tracks the project's external dependency
  (`requests`) for reproducibility.

## Setup

```bash
python -m venv venv
source venv/bin/activate   # macOS/Linux
venv\Scripts\activate      # Windows

pip install -r requirements.txt
```

## Running the scripts

```bash
python generate_log.py
python fetch_data.py
```

Both scripts wrap their logic in `if __name__ == "__main__":` so they
can be run directly from the command line or imported as modules
without side effects.

## Updating dependencies

After installing any new package:

```bash
pip freeze > requirements.txt
