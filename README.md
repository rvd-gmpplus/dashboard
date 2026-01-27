# GMP+ OGSM Dashboard

A simple, visual dashboard for monitoring the 8 KPIs from the OGSM 2026-2028.

![Dashboard Preview](preview.png)

## Versions

The dashboard comes in two versions:

| Version | Description | Best for |
|---------|-------------|----------|
| **V1 - Classic** | Simple donut charts for all 8 KPIs | Quick monthly snapshots |
| **V2 - Historic Data** | Date slider, line charts for certificates growth | Tracking trends over time |

## Features

### V1 - Classic
- **Doughnut charts** with automatic colour coding (green/orange/red)
- **Drag & drop** CSV upload
- **Download template** button built in
- **GMP+ brand style** (purple #6859A7, green #8DC63F)
- **Responsive** design
- **Print-friendly**
- **Works offline** - no server required

### V2 - Historic Data (NEW)
- All V1 features, plus:
- **Date slider** to browse historic data by month
- **Line charts** for FSA and FRA certificates growth
- **Trend visualisation** showing progress towards targets
- **Grouped layout** - donuts together, charts together

## Quick start

### V1 (Classic)
1. Open `index-v1.html` in your browser
2. Download `kpi-data-template.csv` or use the built-in template
3. Drag the CSV to the upload area
4. Done!

### V2 (Historic Data)
1. Open `index-v2.html` in your browser
2. Download `kpi-data-template-v2.csv` or use the built-in template
3. Add your historic data (grouped by date)
4. Drag the CSV to the upload area
5. Use the date slider to browse through time!

## Files

| File | Description |
|------|-------------|
| `index.html` | Landing page (redirects to V1) |
| `index-v1.html` | V1 Dashboard - Classic |
| `index-v2.html` | V2 Dashboard - Historic Data |
| `kpi-data-template.csv` | CSV template for V1 |
| `kpi-data-template-v2.csv` | CSV template for V2 (with dates) |
| `kpi-data-template.xlsx` | Excel template for V1 |
| `INSTRUCTIONS.md` | Detailed guide |

## CSV Format

### V1 Format (without dates)
```csv
id,name,description,category,currentValue,targetValue,unit,type,trend
data-accuracy,Data Accuracy,Description,Tech & Data,72,90,%,percentage,up
```

### V2 Format (with dates)
```csv
date,id,name,description,category,currentValue,targetValue,unit,type,trend
Jan 2025,data-accuracy,Data Accuracy,Description,Tech & Data,68,90,%,percentage,up
Jan 2025,automated-data-entry,Automated Data Entry,Description,Tech & Data,15,33,%,percentage,up
...
Feb 2025,data-accuracy,Data Accuracy,Description,Tech & Data,70,90,%,percentage,up
Feb 2025,automated-data-entry,Automated Data Entry,Description,Tech & Data,17,33,%,percentage,up
...
```

**Important for V2:** Group all 8 KPIs for each date together, then move to the next date.

### Columns

| Column | Required | Description |
|--------|----------|-------------|
| `date` | V2 only | Month and year (e.g., "Jan 2025") |
| `id` | Yes | Unique identification |
| `name` | Yes | Name of the KPI |
| `description` | No | Brief description |
| `category` | No | Category (default: "General") |
| `currentValue` | Yes | Current value |
| `targetValue` | Yes | Target value 2028 |
| `unit` | No | Unit: `%`, `/5`, or empty |
| `type` | No | `percentage`, `rating`, or `number` |
| `trend` | No | `up`, `down`, or `stable` |

## The 8 KPIs

| KPI | Target 2028 | Category | Display |
|-----|-------------|----------|---------|
| Data Accuracy | 90% | Tech & Data | Donut |
| Automated Data Entry | 33% | Tech & Data | Donut |
| CB Satisfaction | 4.0/5 | Tech & Data | Donut |
| Employee Satisfaction | 4.0/5 | Tech & Data | Donut |
| AI Helpdesk Automation | 10% | Tech & Data | Donut |
| FSA Certificates Growth | +4,071 | Markets | Line chart (V2) |
| FRA Certificates Growth | +1,850 | Sustainability | Line chart (V2) |
| Engagement Score | 4.0/5 | Culture | Donut |

## Colour coding

| Colour | Meaning | When |
|--------|---------|------|
| Green | On track | ≥80% of target achieved |
| Orange | Attention needed | 50-80% of target achieved |
| Red | Behind schedule | <50% of target achieved |

## Monthly workflow (V2)

1. Open `kpi-data-template-v2.csv` or your Excel file
2. Add a new block of 8 rows for the current month
3. Fill in the `date` column (e.g., "Apr 2025")
4. Update all `currentValue` and `trend` fields
5. Export as CSV
6. Open V2 dashboard and drag the CSV
7. Use the slider to compare months!

## Switching between versions

Both V1 and V2 have a **version switcher dropdown** in the top-right corner. Click it to switch between versions at any time.

## Technical details

- Pure HTML/CSS/JavaScript - no dependencies
- Works in all modern browsers (Chrome, Edge, Firefox, Safari)
- No server or installation required
- Data stays local (privacy-friendly)

## Support

Contact IT (Rick) for technical support.

---

*GMP+ International © 2026*
