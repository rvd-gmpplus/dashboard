# GMP+ OGSM Dashboard

A simple, visual dashboard for monitoring the 8 KPIs from the OGSM 2026-2028.

![Dashboard Preview](preview.png)

## Features

- **Doughnut charts** with automatic colour coding (green/orange/red)
- **Drag & drop** CSV upload
- **Download template** button built in
- **GMP+ brand style** (purple #6859A7, green #8DC63F)
- **Responsive** design
- **Print-friendly**
- **Works offline** - no server required

## Quick start

1. Download `index.html`
2. Download `kpi-data-template.xlsx` or `kpi-data-template.csv`
3. Open the HTML in your browser
4. Drag the CSV to the upload area
5. Done!

## Files

| File | Description |
|------|-------------|
| `index.html` | The dashboard (open in browser) |
| `kpi-data-template.xlsx` | Excel template to work in |
| `kpi-data-template.csv` | CSV template for direct testing |
| `INSTRUCTIONS.md` | Detailed guide |

## Monthly workflow

1. Open `kpi-data-template.xlsx` in Excel
2. Update column E (`currentValue`) with new values
3. Update column I (`trend`): `up`, `down`, or `stable`
4. Export as CSV (File → Save As → CSV UTF-8)
5. Drag the CSV to the dashboard
6. Present at the team meeting!

## The 8 KPIs

| KPI | Target 2028 | Category |
|-----|-------------|----------|
| Data Accuracy | 90% | Tech & Data |
| Automated Data Entry | 33% | Tech & Data |
| CB Satisfaction | 4.0/5 | Tech & Data |
| Employee Satisfaction | 4.0/5 | Tech & Data |
| AI Helpdesk Automation | 10% | Tech & Data |
| FSA Certificates Growth | +4,071 | Markets |
| FRA Certificates Growth | +1,850 | Sustainability |
| Engagement Score | 4.0/5 | Culture |

## Colour coding

| Colour | Meaning | When |
|--------|---------|------|
| Green | On track | ≥80% of target achieved |
| Orange | Attention needed | 50-80% of target achieved |
| Red | Behind schedule | <50% of target achieved |

## CSV format

```csv
id,name,description,category,currentValue,targetValue,unit,type,trend
data-accuracy,Data Accuracy,Description,Tech & Data,72,90,%,percentage,up
```

### Columns

| Column | Required | Description |
|--------|----------|-------------|
| `id` | Yes | Unique identification |
| `name` | Yes | Name of the KPI |
| `description` | No | Brief description |
| `category` | No | Category (default: "General") |
| `currentValue` | Yes | Current value |
| `targetValue` | Yes | Target value 2028 |
| `unit` | No | Unit: `%`, `/5`, or empty |
| `type` | No | `percentage`, `rating`, or `number` |
| `trend` | No | `up`, `down`, or `stable` |

## Technical details

- Pure HTML/CSS/JavaScript - no dependencies
- Works in all modern browsers (Chrome, Edge, Firefox, Safari)
- No server or installation required
- Data stays local (privacy-friendly)

## Support

Contact IT (Rick) for technical support.

---

*GMP+ International © 2026*
