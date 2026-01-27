# 📊 GMP+ OGSM Dashboard

Een eenvoudig, visueel dashboard voor het monitoren van de 8 KPI's uit de OGSM 2026-2028.

![Dashboard Preview](preview.png)

## ✨ Features

- 🍩 **Donut charts** met automatische kleurcodering (groen/oranje/rood)
- 📁 **Drag & drop** CSV upload
- 📥 **Download template** knop ingebouwd
- 🎨 **GMP+ huisstijl** (paars #6859A7, groen #8DC63F)
- 📱 **Responsive** design
- 🖨️ **Print-vriendelijk**
- 💾 **Werkt offline** - geen server nodig

## 🚀 Snel starten

1. Download `ogsm-dashboard.html`
2. Download `kpi-data-template.xlsx` of `kpi-data-template.csv`
3. Open de HTML in je browser
4. Sleep de CSV naar het upload-vak
5. ✅ Klaar!

## 📁 Bestanden

| Bestand | Beschrijving |
|---------|--------------|
| `ogsm-dashboard.html` | Het dashboard (open in browser) |
| `kpi-data-template.xlsx` | Excel template om in te werken |
| `kpi-data-template.csv` | CSV template voor direct testen |
| `INSTRUCTIES.md` | Uitgebreide handleiding |

## 📅 Maandelijkse workflow

1. Open `kpi-data-template.xlsx` in Excel
2. Pas kolom E (`currentValue`) aan met nieuwe waarden
3. Pas kolom I (`trend`) aan: `up`, `down`, of `stable`
4. Exporteer als CSV (Bestand → Opslaan als → CSV UTF-8)
5. Sleep de CSV naar het dashboard
6. Presenteer in de team meeting! 🎯

## 🎯 De 8 KPI's

| KPI | Doel 2028 | Categorie |
|-----|-----------|-----------|
| Data Accuracy | 90% | Tech & Data |
| Geautomatiseerde Data Entry | 33% | Tech & Data |
| CB Tevredenheid | 4.0/5 | Tech & Data |
| Medewerker Tevredenheid | 4.0/5 | Tech & Data |
| AI Helpdesk Automatisering | 10% | Tech & Data |
| FSA Certificaten Groei | +4.071 | Markets |
| FRA Certificaten Groei | +1.850 | Sustainability |
| Engagement Score | 4.0/5 | Culture |

## 🎨 Kleurcodering

| Kleur | Betekenis | Wanneer |
|-------|-----------|---------|
| 🟢 Groen | Op schema | ≥80% van doel behaald |
| 🟠 Oranje | Aandacht nodig | 50-80% van doel behaald |
| 🔴 Rood | Achter op schema | <50% van doel behaald |

## 📝 CSV formaat

```csv
id,name,description,category,currentValue,targetValue,unit,type,trend
data-accuracy,Data Accuracy,Beschrijving,Tech & Data,72,90,%,percentage,up
```

### Kolommen

| Kolom | Verplicht | Beschrijving |
|-------|-----------|--------------|
| `id` | ✅ | Unieke identificatie |
| `name` | ✅ | Naam van de KPI |
| `description` | ❌ | Korte beschrijving |
| `category` | ❌ | Categorie (default: "Algemeen") |
| `currentValue` | ✅ | Huidige waarde |
| `targetValue` | ✅ | Doelwaarde 2028 |
| `unit` | ❌ | Eenheid: `%`, `/5`, of leeg |
| `type` | ❌ | `percentage`, `rating`, of `number` |
| `trend` | ❌ | `up`, `down`, of `stable` |

## 🔧 Technische details

- Pure HTML/CSS/JavaScript - geen dependencies
- Werkt in alle moderne browsers (Chrome, Edge, Firefox, Safari)
- Geen server of installatie nodig
- Data blijft lokaal (privacy-vriendelijk)

## 📞 Support

Neem contact op met IT (Rick) voor technische ondersteuning.

---

*GMP+ International © 2026*
