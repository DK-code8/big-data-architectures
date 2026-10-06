# Big Data Architectures: Stock Tick Stream Server

TCP socket server that simulates a real-time stock market feed. It emits JSON ticks
(`TICK`, `PRICE`, `TS`) for 24 tickers with random price moves every 2–5 seconds. It serves as the
streaming source for a big-data streaming pipeline (e.g. Spark Structured Streaming reading from a socket).

**Course:** Big Data Architectures, Deree – The American College of Greece (Winter 2025)

## Tech
Python (standard library: `socket`, `datetime`, `random`)

## How to run
```bash
python server.py          # listens on port 9999
```
Connect a consumer, e.g. `nc localhost 9999` or a Spark `socket` source on `localhost:9999`.
