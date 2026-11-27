# ARCA Customs Exchange Rates API — arcamaria-exchange-rate

[![npm version](https://img.shields.io/npm/v/arcamaria-exchange-rate.svg)](https://www.npmjs.com/package/arcamaria-exchange-rate)
[![license](https://img.shields.io/npm/l/arcamaria-exchange-rate.svg)](https://github.com/AllRates-Today/arcamaria-exchange-rate/blob/main/LICENSE)
[![zero dependencies](https://img.shields.io/badge/dependencies-0-brightgreen.svg)](https://www.npmjs.com/package/arcamaria-exchange-rate)
[![TypeScript](https://img.shields.io/badge/TypeScript-types%20included-3178C6.svg)](https://www.typescriptlang.org/)
[![USD/ARS today](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fallratestoday.com%2Fapi%2Fopen%2Fcentral-bank%2Farcamaria%3Fsource%3DUSD%26target%3DARS&query=%24.rate&label=USD%2FARS%20official%2C%20ARCA%20Customs&color=0A7E8C&cacheSeconds=3600)](https://allratestoday.com/tax-authority-rates-api/arcamaria/)
[![rate date](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fallratestoday.com%2Fapi%2Fopen%2Fcentral-bank%2Farcamaria%3Fsource%3DUSD%26target%3DARS&query=%24.rate_date&label=rate%20date&color=555&cacheSeconds=3600)](https://allratestoday.com/tax-authority-rates-api/arcamaria/)

**Official ARCA Customs (Argentina) daily exchange rates for Node.js and TypeScript. The published tax authority rates behind tax filings, customs valuations, audits, and compliant invoicing — not market estimates, but the numbers ARCA Customs itself prints, every business day.**

## 🚀 Why this client?

- 🏛️ **Official rates** — ARCA Customs's own table, with the publisher's own `rate_date` on every response
- 📅 **History back to 1993** — point-in-time tables and daily series for any past date
- 🔀 **Official vs derived, always flagged** — computed inverse/cross pairs carry `derived: true`, never mixed with official prints
- ⚡ **Zero dependencies** — pure ESM + CJS over global `fetch`; Node 18+, Bun, Deno, and edge runtimes
- 🔷 **Type-safe** — full TypeScript definitions shipped with the package
- 🧾 **Compliance-grade metadata** — `rate_type`, publication date, and source disclaimer on every response

> **Official rate, not mid-market:** every value here is a number ARCA Customs itself published, fixed once printed and carrying the tax authority's own `rate_date` — what filings and audits require. Need the live mid-market rate for pricing or display instead? Use the [mid-market API](https://allratestoday.com/docs/) or [`@allratestoday/sdk`](https://www.npmjs.com/package/@allratestoday/sdk). The two can diverge by several percent.

## 🔑 Get your API key

Get a free API key at [allratestoday.com/register](https://allratestoday.com/register) — no credit card required. Latest rates are on every plan, including free.

## 📈 Latest official table

[![Latest ARCA Customs table](https://allratestoday.com/api/open/central-bank/arcamaria/table.svg)](https://allratestoday.com/tax-authority-rates-api/arcamaria/)

The image is rendered live from the keyless endpoint, so it follows the tax authority's publications on npm and on GitHub alike without a new release. The same table as text is folded below for search and copy-paste: on GitHub [a daily Action](.github/workflows/daily-table.yml) refreshes it whenever the tax authority publishes a new table; on npm it is as of the package's publish date.

<!-- daily-table:start -->
<details>
<summary>Table as text: published 2026-11-26 by ARCA Customs — 50 rates. Updated 2026-11-27.</summary>

| Base | Quote | Type | Rate |
| --- | --- | --- | ---: |
| ANG | ARS | buy | 894.692737 |
| ANG | ARS | sell | 894.692737 |
| AUD | ARS | buy | 1054.0758 |
| AUD | ARS | sell | 1063.2359 |
| BOB | ARS | buy | 135.033727 |
| BOB | ARS | sell | 135.033727 |
| BRL | ARS | buy | 278.497522 |
| BRL | ARS | sell | 278.497522 |
| CAD | ARS | buy | 1117.460682 |
| CAD | ARS | sell | 1125.454103 |
| CHF | ARS | buy | 1907.781188 |
| CHF | ARS | sell | 1921.154619 |
| CLP | ARS | buy | 1.537494 |
| CLP | ARS | sell | 1.537494 |
| CNY | ARS | buy | 234.024287 |
| CNY | ARS | sell | 245.725501 |
| COP | ARS | buy | 0.451957 |
| COP | ARS | sell | 0.451957 |
| CZK | ARS | buy | 71.827417 |
| CZK | ARS | sell | 71.827417 |
| DKK | ARS | buy | 233.316076 |
| DKK | ARS | sell | 236.213972 |
| EUR | ARS | buy | 1745.2208 |
| EUR | ARS | sell | 1759.0876 |
| GBP | ARS | buy | 2086.4935 |
| GBP | ARS | sell | 2103.0898 |
| ILS | ARS | buy | 482.583017 |
| ILS | ARS | sell | 482.583017 |
| JPY | ARS | buy | 9.991167 |
| JPY | ARS | sell | 10.0652 |
| MXN | ARS | buy | 81.223088 |
| MXN | ARS | sell | 81.223088 |
| NOK | ARS | buy | 162.787322 |
| NOK | ARS | sell | 165.266347 |
| NZD | ARS | buy | 876.50095 |
| NZD | ARS | sell | 876.50095 |
| PEN | ARS | buy | 461.155264 |
| PEN | ARS | sell | 461.155264 |
| PYG | ARS | buy | 0.248491 |
| PYG | ARS | sell | 0.248491 |
| RUB | ARS | buy | 19.512332 |
| RUB | ARS | sell | 19.512332 |
| SEK | ARS | buy | 155.532392 |
| SEK | ARS | sell | 158.006269 |
| USD | ARS | buy | 1592.5 |
| USD | ARS | sell | 1601.5 |
| UYU | ARS | buy | 39.359726 |
| UYU | ARS | sell | 39.359726 |
| ZAR | ARS | buy | 91.300382 |
| ZAR | ARS | sell | 91.300382 |

</details>

Source: [Official rates published by ARCAMARIA, served by AllRatesToday](https://allratestoday.com/tax-authority-rates-api/arcamaria/). Rates are as printed by the tax authority; AllRatesToday is not affiliated with it.
<!-- daily-table:end -->

## 📦 Installation

```bash
npm install arcamaria-exchange-rate
```

```bash
yarn add arcamaria-exchange-rate
```

```bash
pnpm add arcamaria-exchange-rate
```

Requires Node 18+ (global `fetch`); also runs on Bun, Deno and edge runtimes. Also published under the org scope as [`@allratestoday/arcamaria-exchange-rate`](https://www.npmjs.com/package/@allratestoday/arcamaria-exchange-rate) — same code, same versions.

## 🏁 Quick start

```js
import { getRate } from 'arcamaria-exchange-rate';

const pair = await getRate('USD', 'ARS', { apiKey: 'art_live_...' });
console.log(pair.rate, pair.rate_date); // the official ARCA Customs rate, on the tax authority's own date
```

## 📚 API reference

- [Latest pair rate](#latest-pair-rate) — one pair from the latest official table
- [Full official table](#full-official-table) — everything the tax authority printed, in one call
- [Table for a date](#table-for-a-date) — the official table for an invoice or filing date
- [Daily time series](#daily-time-series) — one pair across a date range

---

### Latest pair rate

Free plan and up. Pairs the tax authority does not print directly are resolved from its table and flagged (see *Official vs derived rates* below).

```js
const pair = await getRate('USD', 'ARS', { apiKey: 'art_live_...' });
```

**Response:**

```javascript
{
  bank: 'arcamaria',
  name: 'ARCA Customs',
  rate_date: '2026-11-24',   // ARCA Customs's own publication date
  source: 'USD',
  target: 'ARS',
  rate: 1593,
  rate_type: 'sell',
  derived: false,
  method: 'published',
  disclaimer: 'Official rates as published by the named central bank. On weekends/holidays the most recent published rate_date is returned.'
}
```

### Full official table

Free plan and up. The complete table for the latest publication date.

```js
import { getLatestRates } from 'arcamaria-exchange-rate';

const table = await getLatestRates({ apiKey: 'art_live_...' });
console.log(table.rate_date, table.rates.length);
```

**Response:**

```javascript
{
  bank: 'arcamaria',
  name: 'ARCA Customs',
  rate_date: '2026-11-24',
  rates: [
    { "base": "USD", "quote": "ARS", "type": "sell", "value": 1593 },
    { "base": "USD", "quote": "ARS", "type": "buy", "value": 1584 },
    // … the rest of the official table (25 currencies vs ARS)
  ],
  disclaimer: '…'
}
```

### Table for a date

Paid plans. The official table for any date since 1993 — weekends and holidays return the most recent published date, flagged via `published_on_requested_date`, which is exactly the in-force rate a filing needs.

```js
import { getRatesForDate } from 'arcamaria-exchange-rate';

const day = await getRatesForDate('2026-06-30', { apiKey: 'art_live_...' });
// Optionally narrow to one pair:
const one = await getRatesForDate('2026-06-30', { apiKey: 'art_live_...', source: 'USD', target: 'ARS' });
```

**Response:**

```javascript
{
  bank: 'arcamaria',
  requested_date: '2026-06-30',
  rate_date: '2026-06-30',                // the date actually published
  published_on_requested_date: true,      // false when a weekend/holiday fell back
  rates: [ /* the full table for that date */ ],
  disclaimer: '…'
}
```

### Daily time series

Paid plans. One resolved rate per publication date — ready for charting, revaluation runs, or audit workpapers.

```js
import { getHistory } from 'arcamaria-exchange-rate';

const series = await getHistory(
  { source: 'USD', target: 'ARS', from: '2026-01-01', to: '2026-11-24' },
  { apiKey: 'art_live_...' }
);
```

**Response:**

```javascript
{
  bank: 'arcamaria',
  source: 'USD',
  target: 'ARS',
  from: '2026-01-01',
  to: '2026-11-24',
  count: 152,
  rates: [
    // one entry per publication date
    { date: '2026-11-24', rate: 1593, rate_type: 'sell', derived: false, method: 'published' },
    // …
  ],
  disclaimer: '…'
}
```

Pass `{ symbol: 'USD' }` instead of `source`/`target` to get the raw published rows for one currency (all rate types, no pair resolution).

---

## 🗺️ Currencies covered

ARCA Customs currently publishes rates covering **25 currencies** against the ARS (as of the latest table):

`ANG` · 🇦🇺 `AUD` · 🇧🇴 `BOB` · 🇧🇷 `BRL` · 🇨🇦 `CAD` · 🇨🇭 `CHF` · 🇨🇱 `CLP` · 🇨🇳 `CNY` · 🇨🇴 `COP` · 🇨🇿 `CZK` · 🇩🇰 `DKK` · 🇪🇺 `EUR` · 🇬🇧 `GBP` · 🇮🇱 `ILS` · 🇯🇵 `JPY` · 🇲🇽 `MXN` · 🇳🇴 `NOK` · 🇳🇿 `NZD` · 🇵🇪 `PEN` · 🇵🇾 `PYG` · 🇷🇺 `RUB` · 🇸🇪 `SEK` · 🇺🇸 `USD` · 🇺🇾 `UYU` · 🇿🇦 `ZAR`

## 🏛️ Source

The exchange rates loaded in Argentina's customs computer system (ARCA / Dirección General de Aduanas, Sistema MARIA) for each day, seller and buyer, in pesos per unit. Customs uses them to convert the declared value of goods and the duties owed into pesos.

- Publisher's own page: [Customs system exchange rates (Cotizaciones María)](https://serviciosweb.afip.gob.ar/aduana/cotizacionesMaria/default.asp) · [serviciosweb.afip.gob.ar](https://serviciosweb.afip.gob.ar/)
- Publication: every business day; the exact schedule, freshness status and any current delay are on the [ARCA Customs rates page](https://allratestoday.com/tax-authority-rates-api/arcamaria/)
- Values are stored unmodified, with the publisher's own `rate_date` on every row — see the [methodology](https://allratestoday.com/official-rates-methodology/)

## 🧭 Reading the numbers

- `value` is always **quote currency per 1 unit of base currency** (`base: "EUR", quote: "USD", value: 1.15` means 1 EUR = 1.15 USD).
- ARCA Customs quotes **ARS per 1 unit of foreign currency** (e.g. `base: "USD", quote: "ARS"` means ARS per one US dollar).
- Need the other way round? Ask `getRate(target, source)` and the API inverts or crosses for you, flagged `derived: true` — never divide a published rate yourself in a compliance workflow.
- `rate_type` tells you which of the tax authority's series a row belongs to (`sell` here); some publishers print buy/sell or several fixings for the same pair.

## 🧩 ERP & accounting systems

Loading the official ARCA Customs rate into an accounting system is a supported workflow, not a hack. Step-by-step guides with the direction each system expects:

- [Dynamics 365 Business Central](https://allratestoday.com/docs/integrations/business-central/) — built-in Currency Exchange Rate Service, no code
- [Xero](https://allratestoday.com/docs/integrations/xero/) · [QuickBooks Online](https://allratestoday.com/docs/integrations/quickbooks/) · [SAP S/4HANA and ECC](https://allratestoday.com/docs/integrations/sap/) · [Odoo](https://allratestoday.com/docs/integrations/odoo/)

The same keyed endpoints return `?format=csv`, `?format=xml` and `?format=xlsx`, and accept the key as `?api_key=` on the URL for importers that cannot send headers:

```bash
curl "https://allratestoday.com/api/v1/central-bank/arcamaria/latest?format=xml&api_key=art_live_..."
```

## 🤖 AI agents

- MCP server: `npx -y @allratestoday/central-bank-mcp` (stdio) or the hosted endpoint `https://allratestoday.com/api/mcp` — tools for official rates, history, cross-bank comparison and publication calendars
- Already using the general SDK or MCP server? Since 2026-10-01 [`@allratestoday/sdk`](https://www.npmjs.com/package/@allratestoday/sdk) 1.4+ has `officialRates('arcamaria')` and [`@allratestoday/mcp-server`](https://www.npmjs.com/package/@allratestoday/mcp-server) 0.6+ has a `get_official_rates` tool — both return this source's latest table with no key, so you can add it without a second dependency
- Claude Code plugin (no key): `/plugin marketplace add AllRates-Today/claude-code-plugin` then `/plugin install allratestoday@allratestoday` — bundles both MCP servers plus an `/official-rate arcamaria ...` command
- Evaluating? Agents can self-issue a trial key with no signup: `POST https://allratestoday.com/api/agent/keys` (send `Content-Type: application/json`) returns a 100-call key valid 7 days that covers the free-plan methods (latest table, pairs); dated tables and history need a [paid plan](https://allratestoday.com/pricing/). The MCP servers expose it as `request_trial_key`
- Machine-readable site guide: [llms.txt](https://allratestoday.com/llms.txt) · [for-ai-agents](https://allratestoday.com/for-ai-agents/)

## ⚖️ Official vs derived rates

If ARCA Customs does not print a pair directly, the API resolves it from the tax authority's own table and says so — official and computed values are never confused:

| `method` | `derived` | Meaning |
| --- | --- | --- |
| `published` | `false` | The tax authority printed this pair directly |
| `inverse` | `true` | Computed as 1 ÷ the published opposite direction |
| `cross` | `true` | Computed via ARS from two published rates |

## 🛡️ Error handling

Errors are thrown as `Error` with `status` (HTTP code) and `body` (the API's JSON error) attached:

```js
try {
  const pair = await getRate('USD', 'XXX', { apiKey: 'art_live_...' });
} catch (err) {
  console.log(err.message); // human-readable reason
  console.log(err.status);  // e.g. 404
}
```

| Status | Meaning |
| ------ | ------- |
| — | Missing `apiKey` (thrown before any request) |
| `400` | Malformed date or parameters |
| `401` | Invalid API key |
| `403` | Endpoint needs a [paid plan](https://allratestoday.com/pricing/) (historical dates & series) |
| `404` | Pair or date range not covered by ARCA Customs |
| `429` | Monthly quota exceeded |

## 🔷 TypeScript

Full definitions ship with the package — no `@types` install:

```ts
import type { LatestRates, PairRate, DatedRates, RateEntry, HistoryQuery, RequestOptions } from 'arcamaria-exchange-rate';
```

## 📦 CommonJS

```javascript
const { getRate } = require('arcamaria-exchange-rate');

getRate('USD', 'ARS', { apiKey: 'art_live_...' }).then((pair) => console.log(pair.rate));
```

## 💡 Quota tips

- Rates change once per business day — cache the official table locally and a small monthly quota goes a long way.
- Every request counts toward your AllRatesToday quota, shared across all AllRatesToday endpoints on your key.

## 📖 Methods reference

| Method | Plan | Description |
| ------ | ---- | ----------- |
| `getRate(source, target, { apiKey })` | Free | Latest rate for one pair, resolved from the official table |
| `getLatestRates({ apiKey })` | Free | The tax authority's full latest official table |
| `getRatesForDate(date, { apiKey, source?, target? })` | Paid | The official table (or one pair) for a YYYY-MM-DD date |
| `getHistory({ symbol \| source+target, from?, to? }, { apiKey })` | Paid | Daily series since 1993 |

## 📥 Bulk data (no key)

Need the whole archive rather than an API call? The same official tables are mirrored daily as open data:

- Hugging Face: [AllRatesToday/central-bank-exchange-rates](https://huggingface.co/datasets/AllRatesToday/central-bank-exchange-rates) — one CSV per institution (`rates/arcamaria.csv`)
- Kaggle: [allratestoday/central-bank-exchange-rates](https://www.kaggle.com/datasets/allratestoday/central-bank-exchange-rates)
- Raw JSON on GitHub: `https://raw.githubusercontent.com/AllRates-Today/central-bank-exchange-rates/main/data/arcamaria/latest.json`

## 🔗 Links

- **Website:** [allratestoday.com](https://allratestoday.com)
- [ARCA Customs rates page](https://allratestoday.com/tax-authority-rates-api/arcamaria/) — live table, publication cadence, FAQ
- [All tax authority sources](https://allratestoday.com/tax-authority-rates-api/) · [Full list of 120+ central banks and 50+ tax authorities](https://allratestoday.com/central-bank-rates-api/institutions/) — one API, the same response shape for every source
- [Download central bank rates](https://allratestoday.com/download-central-bank-rates/) — every bank's latest table and history as Excel, CSV or JSON
- [Bank Exchange Rate API](https://allratestoday.com/bank-exchange-rate-api/) — live buy and sell rates from 1,200+ commercial banks in 120+ countries · [npm](https://www.npmjs.com/package/bank-exchange-rates) · [GitHub](https://github.com/AllRates-Today/bank-exchange-rates)
- [Package docs on the site](https://allratestoday.com/docs/sdk/arcamaria-exchange-rate/) · [ERP integration guides](https://allratestoday.com/docs/integrations/)
- [API documentation](https://allratestoday.com/docs/#central-bank) · [Interactive reference](https://allratestoday.com/api-reference/) · [Methodology](https://allratestoday.com/official-rates-methodology/)
- [Register (Free)](https://allratestoday.com/register) · [Dashboard](https://allratestoday.com/profile) · [Pricing](https://allratestoday.com/pricing/)
- [Status](https://allratestoday.com/status)
- [Postman collection](https://allratestoday.com/postman/)
- [ChatGPT app](https://chatgpt.com/plugins/plugin_asdk_app_6ae1e76098f48191a285ac3f5ab7a83b) — ask ChatGPT for live and official central bank rates
- [OpenAPI reference on Bump.sh](https://bump.sh/allratestoday/doc/allratestoday-api) — also on [SwaggerHub](https://app.swaggerhub.com/apis-docs/allratestoday/allratestoday-exchange-rate-central-bank-rates-api/2.2.0)
- [GitHub](https://github.com/AllRates-Today/arcamaria-exchange-rate)

## 📜 License

MIT
