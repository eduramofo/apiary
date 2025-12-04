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

# Updates the repository and sets all
# submodules to the stable versions currently 
git pull origin main
git submodule update --remote --merge
# Config alias
git config --global alias.upall '!if [ -n "$(git status --porcelain)" ]; then echo "🛑 STOP! You have unsaved changes (pending commit or stash). Command cancelled."; exit 1; else echo "✅ Clean! Updating Flux..." && git pull origin main && git submodule update --remote --merge; fi'
# Update all
git upall

# Forces submodules to fetch the absolute latest
# code from their remote branches (e.g., main),
# ignoring the pinned versions in Apiary.
git submodule update --remote
```
