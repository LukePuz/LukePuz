# Hi, I'm Luke

I build autonomous systems at the intersection of quantitative finance and applied AI. Most
of my work runs locally, acts on live data, and is measured against reality rather than a
backtest — I care about whether a system's decisions actually hold up once the outcome exists.

---

### Helios — autonomous trading research system
A multi-agent pipeline that ingests market events (SEC filings, options flow, insider &
congressional trades, news, macro), has local LLMs (Qwen 2.5 7B/72B via Ollama) write
investment theses with calibrated conviction scores, and sizes every position through a
deterministic, unit-tested risk layer that can veto the model. Runs live at small size through
Interactive Brokers. Every decision is logged with its thesis and realized alpha vs. SPY, so
the system's conviction can be evaluated forward — there are no backtests, on purpose: a
general-purpose LLM may have memorized the historical period, so only decisions made before
their outcomes existed count as evidence.
<br>Python · Celery · Postgres · ChromaDB · Ollama · Interactive Brokers · ~28k LOC

### Clash Royale AI — computer vision + reinforcement learning
An agent that plays Clash Royale on a real device. Trains its own OpenCV + PyTorch detectors
and classifiers (cards, troops, tower HP, elixir) from screen capture, then drives a
policy/reward loop that issues moves over ADB. End-to-end perception to decision to control.
<br>Python · PyTorch · OpenCV · ADB/scrcpy

### Momentum Scanner
A live equity scanner that ranks candidates by a composite conviction model over Interactive
Brokers + Polygon market data.
<br>Python · IBKR · Polygon

### Helios Research — retail-facing market-analysis platform (early stage)
A consumer layer on top of Helios's analysis engine (regime detection, filing/flow monitoring,
macro) so retail investors can use what the trading system does internally. First module
(market regime) working end-to-end on live data.

---

Currently a student at Thomas Jefferson High School for Science & Technology (TJHSST),
exploring research in quantitative finance and machine learning.
