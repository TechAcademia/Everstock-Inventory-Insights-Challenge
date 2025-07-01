# Everstock-Inventory-Insights-Challenge
This repo contains synthetic warehouse data so you can design, build, and test a modern inventory &amp; demand-insights web (or mobile) app for Everstock Logistics. Nothing here is tied to real products, customers, or finances.

*Made for the Tech Academia “Intelligent-Inventory” project.*

This repo contains **synthetic** warehouse data so you can design, build, and test a modern inventory & demand-insights web (or mobile) app for **Everstock Logistics**.
Nothing here is tied to real products, customers, or finances.

---

## What’s in the repo?

| Name / Folder             | What it holds                                                                                                                                          |
| ------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **inventory\_master.csv** | 25 parts Everstock keeps in stock.  For each: part number, description, category, current on-hand quantity.                                            |
| **/demand/**              | One CSV per spotlight part (weekly usage for 2024).<br>• `PRT-001.csv` — Steel Beam<br>• `PRT-009.csv` — Bolt Pack<br>• `PRT-015.csv` — Pressure Valve |
| **README.md**             | You’re reading it.  Explains how the numbers link together and how to use them.                                                                        |

---

## How the numbers link together

1. **Current stock**
   See `inventory_master.csv` → `Quantity` column.
   That’s what Everstock has on the shelf today.

2. **Weekly usage**
   Open `/demand/PRT-001.csv` (or 009 / 015).  Each row is **one week** in 2024 with the quantity consumed.

3. **Stock on hand after a week**
   `ending_stock = starting_stock − weekly_usage`
   (Tip: keep it from going below zero.)

4. **Low-stock alert**
   If `ending_stock` drops below your chosen **re-order point** (e.g., 20 units for Steel Beams) trigger an alert or auto-reorder workflow.

5. **Demand trend graph**
   Sum or plot the 52 weekly quantities to show peaks and slow periods.  Use that chart to justify smarter re-order points or safety stock levels.

---

## Quick notes

* Treat all quantities as *units* of a single currency
* The data are entirely fictional and free to remix for learning or demos.
* Please credit **Tech Academia** if you reuse the synthetic CSVs elsewhere.

Have fun and build something that would make Everstock’s warehouse crew (and their engineering clients) smile!
