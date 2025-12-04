# Flux 🌊

**Flux** is a high-performance algorithmic trading ecosystem, designed to orchestrate data ingestion, market analysis, and trade execution.

## 📂 Architecture

The system is modular, ensuring clear separation of concerns:

- **`nectar/`** (Ingestion)
  The data sourcing engine. Connects to exchanges and providers to generate normalized OHLCV candles.

- **`nectar-client/`** (Interface)
  Standardized Python client for consuming market data across the ecosystem.

- **`spectra/`** (The Brain)
  The intelligence core. Processes the *Flux* of data to identify patterns, volatility, and trading signals.

- **`hive/`** (The Workers)
  The bot cluster. Consumes signals from Spectra and manages orders and positions in real-time.

---

## 🚀 Command's

```bash
# To clone the repository including all submodules
git clone --recurse-submodules git@github.com:eduramofo/flux.git

# Set the submodules in the main branch
cd ./{submodules}
git switch main

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
