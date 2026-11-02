# Luke Puzenski

I build autonomous systems for markets. I mostly write Python, and most of it runs locally on my
own hardware. I'm a high school student at Thomas Jefferson High School for Science and
Technology (TJHSST).

---

### [Helios](https://github.com/LukePuz/helios)

Helios is a live LLM trading research system. It tests one question: does the conviction an LLM
states for a trade predict that trade's return?

It watches the market all day. It pulls in SEC filings, options flow, insider and congressional
trades, news, and macro data. Each event goes through local LLMs (Qwen 2.5 7B and 72B, on two
RTX 3090s with Ollama). The models write a thesis and give it a conviction score. A separate risk
layer then sets the position size and the stop. Its rules are fixed in code, and the model can't
override them. Helios trades live at small size through Interactive Brokers.

I only evaluate it going forward. I don't backtest it, because the models were trained on years
of market history. A test on past data would mostly measure memory instead of skill. Every trade
is logged with its thesis and its return against SPY, and I judge it only after the outcome is in.

Python, Celery, Postgres, Ollama, Interactive Brokers.

### Momentum Scanner

It scans stocks live and ranks them by a conviction score. The score is built from Interactive
Brokers and Polygon data.

Python, IBKR, Polygon.

### Helios Research

This is an early-stage research platform. It's a consumer version of the Helios analysis engine,
so regular investors can use what the trading system does inside. The engine covers regime
detection, filing monitoring, flow monitoring, and macro data. So far the market-regime part
works end to end on live data.

---

Right now I'm learning more about machine learning. I'm also working on how to tell whether a
model is actually any good.
