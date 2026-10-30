# India-Stocks-2401-2430-Historical-Data

Institutional Historical 1-Minute Market Data Archive for **India Equities (Constituents 2401 to 2430)** with automated daily cloud capture via GitHub Actions.

---

## 🏛️ Directory Hierarchy

```text
India-Stocks-2401-2430-Historical-Data/
├── .github/workflows/daily_ingest.yml
├── fetch_batch.py
├── README.md
├── <SYMBOL>/
│   └── 1m/
│       ├── README.md
│       └── <YYYY>/
│           └── <MM>/
│               ├── <SYMBOL>_1m_<YYYY-MM-DD>.csv
```

---

## ⏰ 4-Tier Automated Schedule (Mon–Fri)

| Trigger | Time (IST) | Cron (UTC) | Role |
|:---|:---:|:---:|:---|
| **Primary Trigger** | **15:45 IST** | `15 10 * * 1-5` | 15 mins post-market close |
| **Backup Trigger 1** | **16:45 IST** | `15 11 * * 1-5` | 1 hour safety net |
| **Backup Trigger 2** | **17:45 IST** | `15 12 * * 1-5` | 2 hours safety net |
| **Backup Trigger 3** | **18:45 IST** | `15 13 * * 1-5` | 3 hours safety net |

---

## 📦 Constituents (2401 to 2430)

| # | Symbol | Company Name | Yahoo Ticker |
|---|---|---|---|
| 2401 | `THELEELA` | Leela Palaces Hotels & Resorts Limited | `THELEELA.NS` |
| 2402 | `THEMISMED` | Themis Medicare Limited | `THEMISMED.NS` |
| 2403 | `THOMASCOOK` | Thomas Cook  (India)  Limited | `THOMASCOOK.NS` |
| 2404 | `THOMASCOTT` | Thomas Scott (India) Limited | `THOMASCOTT.NS` |
| 2405 | `THYROCARE` | Thyrocare Technologies Limited | `THYROCARE.NS` |
| 2406 | `TI` | Tilaknagar Industries Limited | `TI.NS` |
| 2407 | `TICL` | Twamev Construction and Infrastructure Limited | `TICL.NS` |
| 2408 | `TIGERLOGS` | Tiger Logistics (India) Limited | `TIGERLOGS.NS` |
| 2409 | `TIIL` | Technocraft Industries (India) Limited | `TIIL.NS` |
| 2410 | `TIJARIA` | Tijaria Polypipes Limited | `TIJARIA.NS` |
| 2411 | `TIKONA` | Tikona Communication Limited | `TIKONA.NS` |
| 2412 | `TIL` | TIL Limited | `TIL.NS` |
| 2413 | `TIMETECHNO` | Time Technoplast Limited | `TIMETECHNO.NS` |
| 2414 | `TIMEX` | Timex Group India Limited | `TIMEX.NS` |
| 2415 | `TINNARUBR` | Tinna Rubber and Infrastructure Limited | `TINNARUBR.NS` |
| 2416 | `TIPSFILMS` | Tips Films Limited | `TIPSFILMS.NS` |
| 2417 | `TIPSMUSIC` | Tips Music Limited | `TIPSMUSIC.NS` |
| 2418 | `TIRUMALCHM` | Thirumalai Chemicals Limited | `TIRUMALCHM.NS` |
| 2419 | `TIRUPATIFL` | Tirupati Forge Limited | `TIRUPATIFL.NS` |
| 2420 | `TMB` | Tamilnad Mercantile Bank Limited | `TMB.NS` |
| 2421 | `TNPETRO` | Tamilnadu PetroProducts Limited | `TNPETRO.NS` |
| 2422 | `TNPL` | Tamil Nadu Newsprint & Papers Limited | `TNPL.NS` |
| 2423 | `TNTELE` | Tamilnadu Telecommunication Limited | `TNTELE.NS` |
| 2424 | `TOKYOPLAST` | Tokyo Plast International Limited | `TOKYOPLAST.NS` |
| 2425 | `TOLINS` | Tolins Tyres Limited | `TOLINS.NS` |
| 2426 | `TONBO` | Tonbo Imaging India Limited | `TONBO.NS` |
| 2427 | `TOTAL` | Total Transport Systems Limited | `TOTAL.NS` |
| 2428 | `TOUCHWOOD` | Touchwood Entertainment Limited | `TOUCHWOOD.NS` |
| 2429 | `TOYAMSL` | Toyam Sports Limited | `TOYAMSL.NS` |
| 2430 | `TPHQ` | Teamo Productions HQ Limited | `TPHQ.NS` |


---

## ⚡ 1-Line Pandas Stream Loader

```python
import pandas as pd

# Example: Stream THELEELA 1m data
url = "https://raw.githubusercontent.com/parshant65-lang/India-Stocks-2401-2430-Historical-Data/main/THELEELA/1m/2026/10/THELEELA_1m_2026-10-12.csv"
df = pd.read_csv(url)
print(df.head())
```
