# GMP+ OGSM Dashboard - Instructions

## Overview

This dashboard displays the 8 KPIs from the OGSM 2026-2028 with doughnut charts. You feed the dashboard with a CSV file that you export from Excel.

---

## What do you have?

| File | Purpose |
|------|---------|
| **index.html** | The dashboard - open in your browser |
| **kpi-data-template.xlsx** | Excel template - this is where you work |
| **INSTRUCTIONS.md** | This guide |

---

## How to use

### First time:

1. **Open** `kpi-data-template.xlsx` in Excel
2. Fill in the current values (column E: "currentValue")
3. **Export as CSV**:
   - File → Save As
   - Choose "CSV UTF-8 (Comma delimited)"
   - Name the file e.g. `kpi-january-2026.csv`
4. **Open** `index.html` in your browser
5. **Drag** the CSV file to the dashboard (or click to select)
6. Done!

### Every month:

1. Open your Excel file
2. Update column E (currentValue) with new values
3. Update column I (trend) if needed
4. Export as CSV
5. Drag to the dashboard

---

## Excel columns explained

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

---

## The 8 KPIs

| KPI | Target 2028 | Type | Example value |
|-----|-------------|------|---------------|
| Data Accuracy | 90% | percentage | 72 |
| Automated Data Entry | 33% | percentage | 18 |
| CB Satisfaction | 4.0/5 | rating | 3.8 |
| Employee Satisfaction | 4.0/5 | rating | 3.6 |
| AI Helpdesk Automation | 10% | percentage | 2 |
| FSA Certificates Growth | 4,071 | number | 1250 |
| FRA Certificates Growth | 1,850 | number | 620 |
| Engagement Score | 4.0/5 | rating | 3.9 |

---

## Automatic colours

The dashboard colours automatically based on progress towards the target:

| Colour | Meaning | When |
|--------|---------|------|
| **Green** | On track | ≥80% of target |
| **Orange** | Attention needed | 50-80% of target |
| **Red** | Behind schedule | <50% of target |

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
3,8     ← Comma doesn't work
1.250   ← Full stop as thousands separator doesn't work
Up      ← Capital letter doesn't work
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
- Check that the first row contains the headers: `id,name,description,...`
- Check that there are no empty rows between the data

### Values are not displayed correctly
- Check the decimal separator (full stop, not comma)
- Check that `type` is set correctly

### CSV is not recognised
- Ensure the file ends with `.csv`
- Try exporting again as "CSV UTF-8"

---

## Tips

1. **Backup**: Save a copy of your Excel file each month (`kpi-jan-2026.xlsx`, etc.)
2. **Print**: Ctrl+P (or Cmd+P) in the browser for a print version
3. **Present**: F11 for full screen
4. **Download template**: You can always download a new template from the dashboard

---

## Monthly checklist

- [ ] Open Excel template
- [ ] Update column E (currentValue) for all 8 KPIs
- [ ] Update column I (trend) where needed
- [ ] Export as CSV
- [ ] Open dashboard and drag CSV into it
- [ ] Verify all values are correct
- [ ] Make backup of Excel file

---

## Need help?

Contact IT (Rick) for technical support.

---

*Version 3.0 | January 2026 | GMP+ International*
