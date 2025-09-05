# Farmacias de Chile — GitHub Mirror (daily)

This repo uses **GitHub Actions** to fetch the official MINSAL API and publish two files:
- `farmacias.json` — raw JSON
- `farmacias.csv` — clean CSV with common columns

It runs **daily at 03:00 UTC** and **on demand**.

## Quick start (5 minutes)

1. Create a **new GitHub repository** (public or private), e.g. `farmacias-chile`.
2. Download this ZIP and **extract** it.
3. Drag & drop **all files** into your new repo (or use `git`).
4. Go to **Actions** tab → enable workflows if prompted.
5. Trigger a manual run: **Actions → Fetch farmacias → Run workflow**.
6. After it finishes, access the CSV at:

```
https://raw.githubusercontent.com/<your-username>/<your-repo>/main/farmacias.csv
```

> Replace `<your-username>` and `<your-repo>` accordingly.

## Excel connection (Power Query)

Use **Data → Get Data → From Web** with your raw URL above.
If you prefer the full M code, paste this into **Power Query → Advanced Editor**:

(See `excel_power_query_m.txt` in this repo.)

## Notes

- Source API (documented on Datos.gob.cl): `https://midas.minsal.cl/farmacia_v2/WS/getLocales.php`
- License on Datos.gob.cl entry: **Creative Commons Attribution** (check the catalog page for details).
- If your network blocks `raw.githubusercontent.com`, try **GitHub Pages** instead (you can enable Pages and expose the CSV there).
