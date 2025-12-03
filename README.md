# Apiary 🐝

**Apiary** is a modular ecosystem for algorithmic trading, orchestrating data collection, analysis, and execution.

## 📂 Architecture

The system is composed of four main submodules, organized by the "Hive" metaphor:

- **`nectar/`** (Data Source)
  Responsibility: Market data ingestion and candle generation.

- **`nectar-client/`** (Connector)
  Responsibility: Interface library for consuming market data.

- **`spectra/`** (The Brain)
  Responsibility: Market analysis, pattern recognition, and strategy core.

- **`hive/`** (The Workers)
  Responsibility: Execution bots and order management.

---

## 🚀 Command's

```bash
# To clone the repository including all submodules
git clone --recurse-submodules https://github.com/eduramofo/apiary.git

# Updates the Apiary repository and sets all 
# submodules to the stable versions currently 
# pinned in this project. Use this to ensure 
# your local environment matches the team's stable state.
git pull --recurse-submodules

# Forces submodules to fetch the absolute latest
# code from their remote branches (e.g., main),
# ignoring the pinned versions in Apiary.
git submodule update --remote

# If you have already cloned the repository 
# without the flag, run this to fetch the submodules
git submodule update --init --recursive
```
