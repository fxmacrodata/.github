# FXMacroData 📊

**Real-time central bank & macroeconomic data API for FOREX traders.**

[fxmacrodata.com](https://fxmacrodata.com) provides a standardised, timestamped API that delivers macroeconomic indicators and spot FX prices sourced directly from central banks and statistical agencies — enabling quants, algo traders, and financial developers to build data-driven FOREX strategies without lookahead bias.

---

## 🌐 Services

### Macroeconomic Indicators API

Access 76+ macroeconomic indicators across all major currency pairs, updated in real time from official sources such as the ECB, FRED, and RBA.

**Covered categories:**

| Category | Indicators |
|---|---|
| **Monetary Policy** | Policy rate, interbank rate, overnight deposit rate |
| **Economy** | GDP growth, inflation (CPI/HICP), trade balance, current account balance |
| **Labor Market** | Unemployment rate, employment, full-time/part-time employment, participation rate, non-farm payrolls |
| **Government Bond Yields** | 2y, 3y, 5y, 10y government bond yields, inflation-linked bonds |
| **Other** | Money supply (M3), inflation expectations, house prices |

**Supported currencies:** USD · EUR · GBP · AUD · CAD · JPY · CHF · NZD · NOK

> 💡 **Free USD data** — USD macroeconomic endpoints are available at no cost, with no API key required.

---

### Forex Price Feed API

Free historical and real-time spot FX prices for all major currency pairs. No API key is needed for USD-based queries.

```python
fx = client.get_fx_price("usd", "jpy", start_date="2024-01-01")
```

---

### Python SDK

Install the official Python SDK from PyPI and start fetching data in minutes:

```bash
pip install fxmacrodata
```

**Synchronous usage:**

```python
from fxmacrodata import Client

client = Client(api_key="YOUR_API_KEY")

# Fetch a macroeconomic indicator
data = client.get_indicator("eur", "cpi", start_date="2023-01-01")
print(data)

# Fetch FX spot prices (free, no API key needed for USD pairs)
fx = client.get_fx_price("usd", "gbp", start_date="2024-01-01")
print(fx)
```

**Asynchronous usage:**

```python
import asyncio
from fxmacrodata import AsyncClient

async def main():
    async with AsyncClient(api_key="YOUR_API_KEY") as client:
        data = await client.get_indicator("eur", "cpi")
        print(data)

asyncio.run(main())
```

The SDK integrates seamlessly with **pandas** and **NumPy** for quantitative analysis and model building.

---

## 💡 Key Features

- **No lookahead bias** — every data point includes the exact announcement timestamp, critical for accurate backtesting
- **Real-time updates** — sourced directly from central banks and statistical agencies
- **Free USD data** — access all USD macroeconomic indicators without an API key
- **Free FX price feed** — historical spot prices for major currency pairs at no cost
- **76+ indicators** across major currencies
- **Sync & async clients** — lightweight, depends only on `requests` and `aiohttp`
- **REST API** — full Swagger/OpenAPI documentation available

---

## 💰 Pricing

| Plan | Access |
|---|---|
| **Free** | All USD macroeconomic indicators + full FX price feed |
| **Paid** (from $25/month) | All currencies — 14-day free trial included |

---

## 🔗 Links

- 🌐 **Website:** [fxmacrodata.com](https://fxmacrodata.com)
- 📖 **API Documentation:** [fxmacrodata.com/api-data-docs](https://fxmacrodata.com/api-data-docs/)
- 🔌 **Swagger UI:** [fxmacrodata.com/api/docs](https://fxmacrodata.com/api/docs)
- 📦 **PyPI:** [pypi.org/project/fxmacrodata](https://pypi.org/project/fxmacrodata/)
- 📘 **SDK Docs:** [fxmacrodata.readthedocs.io](https://fxmacrodata.readthedocs.io/en/latest/)
- 🐍 **GitHub SDK:** [github.com/fxmacrodata/fxmacrodata](https://github.com/fxmacrodata/fxmacrodata)
