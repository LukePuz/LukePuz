# Luke Puzenski

I build autonomous systems for markets and games, mostly in Python and mostly running locally
on my own hardware. I'm a high school student at Thomas Jefferson High School for Science and
Technology (TJHSST).

---

### Helios — autonomous trading research system
Helios watches the market all day. It pulls in SEC filings, options flow, insider and
congressional trades, news, and macro data, then runs each event through a pipeline of local
LLMs (Qwen 2.5, 7B and 72B, on two RTX 3090s via Ollama). The models write a thesis and a
conviction score. A separate rule-based risk layer that the model cannot override decides the
actual position size and stop. It trades live at small size through Interactive Brokers.

I don't backtest it. The models were trained on years of market history, so testing them on
the past mostly measures memory instead of skill. Every trade is logged with its thesis and
its return against SPY, and judged only after the outcome is in.

Python, Celery, Postgres, Ollama, Interactive Brokers.

### Clash Royale AI — computer vision and reinforcement learning
An agent that plays Clash Royale on a real phone. I trained the vision models myself with
OpenCV and PyTorch to read cards, troops, tower health, and elixir off screenshots. A policy
then picks moves and sends them to the device over ADB.

Python, PyTorch, OpenCV, ADB.

### Momentum Scanner
Scans stocks live and ranks them with a conviction score built from Interactive Brokers and
Polygon data.

Python, IBKR, Polygon.

### Helios Research — early-stage research platform
A consumer version of Helios's analysis engine (regime detection, filing and flow monitoring,
macro) so regular investors can use what the trading system does internally. The market-regime
piece works end to end on live data so far.

---

Right now I'm going deeper on machine learning and on how to tell whether a model is actually
any good.
