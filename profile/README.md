# FXMacroData 📊

**Official-source macroeconomic and FX data, timestamped for backtesting.**

[fxmacrodata.com](https://fxmacrodata.com) delivers macroeconomic indicators, FX
prices, and central-bank releases sourced directly from central banks and
statistical agencies. Every observation carries the exact announcement
timestamp, so research and backtests can ask *what was knowable at the time*
rather than silently using a revised figure.

---

## 📈 Coverage

**656 indicator endpoints · 97 distinct macroeconomic indicators · 18 currencies**

`AUD` · `BRL` · `CAD` · `CHF` · `CNH` · `CNY` · `DKK` · `EUR` · `GBP` · `ILS` ·
`JPY` · `NGN` · `NOK` · `NZD` · `PEN` · `SEK` · `THB` · `USD`

| Category | Indicators |
|---|---|
| **Monetary policy** | Policy rate, interbank rate, overnight deposit rate |
| **Economy** | GDP growth, inflation (CPI/HICP), trade balance, current account, retail sales |
| **Labour market** | Unemployment, employment, participation rate, non-farm payrolls |
| **Government bonds** | 2y–30y yields, inflation-linked bonds |
| **Positioning & commodities** | CFTC Commitment of Traders, gold, silver, platinum |
| **Other** | Money supply, inflation expectations, house prices |

Browse the full matrix at [Data Coverage](https://fxmacrodata.com/data-coverage).

---

## 🚀 Start here

```bash
pip install fxmacrodata
```

```python
from fxmacrodata import Client

client = Client(api_key="YOUR_API_KEY")

# Macroeconomic releases, with announcement timestamps
data = client.get_indicator("eur", "inflation", start_date="2023-01-01")

# Upcoming releases
calendar = client.get_calendar("usd")
```

An async client is available as `AsyncClient`. Both depend only on `requests`
and `aiohttp`, and work directly with pandas.

---

## 📦 Repositories

| Repo | What it is |
|---|---|
| [**fxmacrodata**](https://github.com/fxmacrodata/fxmacrodata) | Official Python SDK — sync + async clients ([PyPI](https://pypi.org/project/fxmacrodata/)) |
| [**mcp-server-fxmacrodata**](https://github.com/fxmacrodata/mcp-server-fxmacrodata) | MCP server, for using the data from Claude and other AI agents |
| [**examples**](https://github.com/fxmacrodata/examples) | Runnable examples across backtesting and analysis frameworks |
| [**ocaml-fxmacrodata**](https://github.com/fxmacrodata/ocaml-fxmacrodata) | OCaml client ([opam](https://opam.ocaml.org/packages/fxmacrodata/)) |
| [**FXMacroData.jl**](https://github.com/fxmacrodata/FXMacroData.jl) | Julia client |
| [**astrbot-plugin-fxmacrodata**](https://github.com/fxmacrodata/astrbot-plugin-fxmacrodata) | AstrBot plugin exposing the full MCP tool set |

---

## 🤖 AI agents & MCP

The API is available as a hosted **Model Context Protocol** server, so an agent
can query macro data, release calendars, and FX rates as tools:

```
https://mcp.fxmacrodata.com/mcp
```

See the [MCP Server docs](https://fxmacrodata.com/documentation/mcp-server) for
client setup, or run the [self-hosted server](https://github.com/fxmacrodata/mcp-server-fxmacrodata).

---

## 💡 Why it exists

- **No lookahead bias** — every point carries its announcement timestamp, and
  revisions keep their original epochs, so you can reconstruct what was
  published when
- **Official sources only** — central banks and statistical agencies, with
  provenance on every response
- **Release-aware** — a calendar of upcoming releases with confirmed vs assumed
  times, not just historical series
- **Built for machines** — REST, GraphQL, OpenAPI, and MCP

---

## 💰 Access

| Plan | Access |
|---|---|
| **Free** | USD macroeconomic indicators, most recent 90 days, no API key required |
| **Individual** — $50/month | All 18 currencies, full history, FX prices, COT, commodities. 14-day free trial |
| **Enterprise** | Higher limits, commercial redistribution, support |

See [Pricing](https://fxmacrodata.com/pricing) for current terms.

---

## 🔗 Links

- 🌐 **Website:** [fxmacrodata.com](https://fxmacrodata.com)
- 📖 **API reference:** [fxmacrodata.com/documentation/reference](https://fxmacrodata.com/documentation/reference)
- 🔌 **Swagger UI:** [fxmacrodata.com/api/docs](https://fxmacrodata.com/api/docs)
- 📚 **Quickstart & guides:** [fxmacrodata.com/api-data-docs](https://fxmacrodata.com/api-data-docs/)
- 📘 **SDK docs:** [fxmacrodata.readthedocs.io](https://fxmacrodata.readthedocs.io/en/latest/)
- 📊 **Data coverage:** [fxmacrodata.com/data-coverage](https://fxmacrodata.com/data-coverage)
