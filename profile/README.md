# FXMacroData 📊

**Official-source macroeconomic and FX data for research and backtesting.**

[FXMacroData](https://fxmacrodata.com) provides macroeconomic observations, FX
data and central-bank releases sourced from central banks and statistical
agencies. Use supplied publication timestamps and provenance for
point-in-time research.

[Subscribe to FXMacroData](https://fxmacrodata.com/subscribe?utm_source=github&utm_medium=referral&utm_campaign=open_source_integrations&utm_content=org_profile_subscribe) for non-USD data, full available history, FX, commodities and positioning. Use the public USD workflow to evaluate the API before connecting your subscription.

---

## 📈 Coverage

Explore the [current data coverage](https://fxmacrodata.com/data-coverage) for
available currencies, indicators and history.

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

# The key is sent as an X-API-Key header, not in the URL.
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

- **Point-in-time research** — use supplied publication timestamps and revision
  metadata when constructing historical datasets
- **Official sources only** — central banks and statistical agencies, with
  provenance on every response
- **Release-aware** — a calendar of upcoming releases with confirmed vs assumed
  times, not just historical series
- **Built for machines** — REST, GraphQL, OpenAPI, and MCP

---

## 💰 Access

| Plan | Access |
|---|---|
| **Individual** | Subscription for personal research and trading, including non-USD data, full available history, FX, positioning and commodities |
| **Enterprise** | Subscription for institutional use, with team access and administrative controls |
| **USD evaluation** | Public USD macroeconomic data within the public-history window, without an API key |

[Compare subscriptions](https://fxmacrodata.com/subscribe?utm_source=github&utm_medium=referral&utm_campaign=open_source_integrations&utm_content=org_profile_subscribe) for current access and terms. Commercial redistribution is a separate add-on.

---

## 🔌 Endpoint & authentication

All endpoints live under `https://api.fxmacrodata.com/v1/`. Authenticate with an
`X-API-Key` header — an `api_key` query parameter is still accepted, but a key in
a URL is recorded by proxies, CDNs and server access logs.

---

## 🔗 Links

- 🌐 **Website:** [fxmacrodata.com](https://fxmacrodata.com)
- 📖 **API reference:** [fxmacrodata.com/documentation/reference](https://fxmacrodata.com/documentation/reference)
- 🔌 **Swagger UI:** [fxmacrodata.com/api/docs](https://fxmacrodata.com/api/docs)
- 📚 **Quickstart & guides:** [fxmacrodata.com/api-data-docs](https://fxmacrodata.com/api-data-docs/)
- 📘 **SDK docs:** [fxmacrodata.readthedocs.io](https://fxmacrodata.readthedocs.io/en/latest/)
- 📊 **Data coverage:** [fxmacrodata.com/data-coverage](https://fxmacrodata.com/data-coverage)
