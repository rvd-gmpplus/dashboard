# OGSM Dashboard - User Guide

## Overview

The GMP+ OGSM Dashboard visualises the 8 KPIs from the OGSM 2026-2028. It runs entirely in your browser - no installation or server required.

---

## Dashboard Versions

| Version | File | Best for |
|---------|------|----------|
| **V1 - Classic** | `index-v1.html` | Monthly snapshots, simple setup |
| **V2 - Historic Data** | `index-v2.html` | Tracking trends over time |

### V1 Features
- All 8 KPIs as donut charts
- Simple CSV without dates
- Quick to update and present

### V2 Features
- Date slider to browse historic data
- Line charts for FSA and FRA growth
- Grouped layout (donuts together, charts together)
- See trends month-by-month

---

## What do you have?

| File | Purpose |
|------|---------|
| **index.html** | Landing page (redirects to V1) |
| **index-v1.html** | V1 Dashboard |
| **index-v2.html** | V2 Dashboard |
| **kpi-data-template.xlsx** | Excel template for V1 |
| **kpi-data-template.csv** | CSV template for V1 |
| **kpi-data-template-v2.csv** | CSV template for V2 (with dates) |
| **INSTRUCTIONS.md** | This guide |

---

## How to use V1 (Classic)

### First time:

1. **Open** `kpi-data-template.xlsx` in Excel
2. Fill in the current values (column E: "currentValue")
3. **Export as CSV**:
   - File → Save As
   - Choose "CSV UTF-8 (Comma delimited)"
   - Name the file e.g. `kpi-january-2026.csv`
4. **Open** `index-v1.html` in your browser
5. **Drag** the CSV file to the dashboard (or click to select)
6. Done!

### Every month:

1. Open your Excel file
2. Update column E (currentValue) with new values
3. Update column I (trend) if needed
4. Export as CSV
5. Drag to the dashboard

---

## How to use V2 (Historic Data)

### First time:

1. **Open** `kpi-data-template-v2.csv` in Excel
2. You'll see data grouped by date (8 rows per month)
3. **Open** `index-v2.html` in your browser
4. **Drag** the CSV file to the dashboard
5. Use the **date slider** to browse through months!

### Adding a new month:

1. Open your V2 CSV file in Excel
2. Copy the last 8 rows (one complete month)
3. Paste at the bottom of the file
4. Change the `date` column to the new month (e.g., "Apr 2025")
5. Update `currentValue` and `trend` for all 8 KPIs
6. Save as CSV
7. Drag to the dashboard

### V2 CSV structure example:
```csv
date,id,name,description,category,currentValue,targetValue,unit,type,trend
Jan 2025,data-accuracy,Data Accuracy,...,Tech & Data,68,90,%,percentage,up
Jan 2025,automated-data-entry,Automated Data Entry,...,Tech & Data,15,33,%,percentage,up
...8 rows for Jan 2025...
Feb 2025,data-accuracy,Data Accuracy,...,Tech & Data,70,90,%,percentage,up
Feb 2025,automated-data-entry,Automated Data Entry,...,Tech & Data,17,33,%,percentage,up
...8 rows for Feb 2025...
```

---

## Excel/CSV columns explained

### V1 Columns
| Column | Name | Update? | Explanation |
|--------|------|---------|-------------|
| A | id | No | Technical identification |
| B | name | May | Name of the KPI |
| C | description | May | Brief description |
| D | category | May | Category (Tech & Data, Markets, etc.) |
| **E** | **currentValue** | **YES!** | **Current value - update this monthly** |
| F | targetValue | Rarely | Target 2028 (only if target changes) |
| G | unit | Rarely | Unit: %, /5, or empty |
| H | type | No | percentage, rating, or number |
| **I** | **trend** | **YES!** | **up, down, or stable** |

### V2 Additional Column
| Column | Name | Update? | Explanation |
|--------|------|---------|-------------|
| **A** | **date** | **YES!** | Month and year (e.g., "Jan 2025") |

Note: In V2, the other columns shift by one (id becomes column B, etc.)

---

## The 8 KPIs

| KPI | Target 2028 | Type | V2 Display |
|-----|-------------|------|------------|
| Data Accuracy | 90% | percentage | Donut |
| Automated Data Entry | 33% | percentage | Donut |
| CB Satisfaction | 4.0/5 | rating | Donut |
| Employee Satisfaction | 4.0/5 | rating | Donut |
| AI Helpdesk Automation | 10% | percentage | Donut |
| FSA Certificates Growth | 4,071 | number | **Line chart** |
| FRA Certificates Growth | 1,850 | number | **Line chart** |
| Engagement Score | 4.0/5 | rating | Donut |

---

## Automatic colours

The dashboard colours automatically based on progress towards the target:

| Colour | Meaning | When |
|--------|---------|------|
| **Green** | On track | ≥80% of target |
| **Orange** | Attention needed | 50-80% of target |
| **Red** | Behind schedule | <50% of target |

---

## Date format (V2)

Use this format: `Mon YYYY`

**Correct:**
- Jan 2025
- Feb 2025
- Mar 2025
- Dec 2028

**Incorrect:**
- January 2025 (too long)
- 01/2025 (wrong format)
- 2025-01 (wrong format)

---

## Switching between versions

Both V1 and V2 have a **version switcher** dropdown in the top-right corner:
1. Click the dropdown
2. Select the version you want
3. The page will load the selected version

---

## Important notes for data entry

### Correct:
```
3.8     ← Full stop as decimal
1250    ← No thousands separator
up      ← Lower case
```

### Incorrect:
```
3,8     ← Comma may cause issues
1.250   ← Full stop as thousands separator doesn't work
Up      ← Capital letter doesn't work for trend
```

---

## Exporting CSV from Excel

### Windows:
1. File → Save As
2. Browse to desired folder
3. Save as type: **CSV UTF-8 (Comma delimited) (*.csv)**
4. Save

### Mac:
1. File → Export
2. File format: **CSV UTF-8 (.csv)**
3. Export

---

## Troubleshooting

### "No valid KPI data found"
- Check that the first row contains the headers
- Check that there are no empty rows between the data

### Values are not displayed correctly
- Check the decimal separator (full stop, not comma)
- Check that `type` is set correctly

### CSV is not recognised
- Ensure the file ends with `.csv`
- Try exporting again as "CSV UTF-8"

### Date slider not showing (V2)
- Ensure your CSV has a `date` column as the first column
- Check date format: "Jan 2025" not "January 2025"
- You need at least 2 different dates for the slider to appear

### Line charts not showing (V2)
- Check that `fsa-certificates` and `fra-certificates` are in your data
- The ID must match exactly (lower case, with hyphens)

---

## Tips

1. **Backup**: Save a copy of your data file each month
2. **Print**: Ctrl+P (or Cmd+P) in the browser for a print version
3. **Present**: F11 for full screen
4. **Download template**: You can always download a new template from the dashboard

---

## Monthly checklist (V1)

- [ ] Open Excel template
- [ ] Update column E (currentValue) for all 8 KPIs
- [ ] Update column I (trend) where needed
- [ ] Export as CSV
- [ ] Open dashboard and drag CSV into it
- [ ] Verify all values are correct
- [ ] Make backup of Excel file

## Monthly checklist (V2)

- [ ] Open your V2 CSV file
- [ ] Add 8 new rows for the current month
- [ ] Fill in the date column (e.g., "Apr 2025")
- [ ] Update currentValue and trend for all 8 KPIs
- [ ] Save as CSV
- [ ] Open V2 dashboard and drag CSV into it
- [ ] Use the slider to verify all months display correctly
- [ ] Make backup of CSV file

---

## Need help?

Contact IT (Rick) for technical support.

---

*Version 4.0 | January 2026 | GMP+ International*
