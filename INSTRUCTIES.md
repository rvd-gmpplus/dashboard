# 📊 GMP+ OGSM Dashboard - Instructies

## Overzicht

Dit dashboard toont de 8 KPI's uit de OGSM 2026-2028 met donut-diagrammen. Je voedt het dashboard met een CSV-bestand dat je exporteert vanuit Excel.

---

## 📁 Wat heb je?

| Bestand | Doel |
|---------|------|
| **ogsm-dashboard.html** | Het dashboard - open in je browser |
| **kpi-data-template.xlsx** | Excel template - hier werk je in |
| **INSTRUCTIES.md** | Deze handleiding |

---

## 🚀 Hoe te gebruiken

### Eerste keer:

1. **Open** `kpi-data-template.xlsx` in Excel
2. Vul de actuele waarden in (kolom E: "currentValue")
3. **Exporteer als CSV**:
   - Bestand → Opslaan als
   - Kies "CSV UTF-8 (door komma's gescheiden)"
   - Noem het bestand bijv. `kpi-januari-2026.csv`
4. **Open** `ogsm-dashboard.html` in je browser
5. **Sleep** het CSV-bestand naar het dashboard (of klik om te selecteren)
6. ✅ Klaar!

### Elke maand:

1. Open je Excel-bestand
2. Pas kolom E (currentValue) aan met nieuwe waarden
3. Pas kolom I (trend) aan indien nodig
4. Exporteer als CSV
5. Sleep naar het dashboard

---

## 📝 Excel kolommen uitgelegd

| Kolom | Naam | Aanpassen? | Uitleg |
|-------|------|------------|--------|
| A | id | ❌ Nee | Technische identificatie |
| B | name | ✅ Mag | Naam van de KPI |
| C | description | ✅ Mag | Korte beschrijving |
| D | category | ✅ Mag | Categorie (Tech & Data, Markets, etc.) |
| **E** | **currentValue** | **✅ JA!** | **Huidige waarde - dit pas je maandelijks aan** |
| F | targetValue | ⚠️ Zelden | Doel 2028 (alleen bij doelwijziging) |
| G | unit | ⚠️ Zelden | Eenheid: %, /5, of leeg |
| H | type | ❌ Nee | percentage, rating, of number |
| **I** | **trend** | **✅ JA!** | **up, down, of stable** |

---

## 🎯 De 8 KPI's

| KPI | Doel 2028 | Type | Voorbeeldwaarde |
|-----|-----------|------|-----------------|
| Data Accuracy | 90% | percentage | 72 |
| Geautomatiseerde Data Entry | 33% | percentage | 18 |
| CB Tevredenheid | 4.0/5 | rating | 3.8 |
| Medewerker Tevredenheid | 4.0/5 | rating | 3.6 |
| AI Helpdesk Automatisering | 10% | percentage | 2 |
| FSA Certificaten Groei | 4.071 | number | 1250 |
| FRA Certificaten Groei | 1.850 | number | 620 |
| Engagement Score | 4.0/5 | rating | 3.9 |

---

## 🎨 Automatische kleuren

Het dashboard kleurt automatisch op basis van voortgang naar het doel:

| Kleur | Betekenis | Wanneer |
|-------|-----------|---------|
| 🟢 **Groen** | Op schema | ≥80% van het doel |
| 🟠 **Oranje** | Aandacht nodig | 50-80% van het doel |
| 🔴 **Rood** | Achter op schema | <50% van het doel |

---

## ⚠️ Let op bij invoer

### ✅ Goed:
```
3.8     ← Punt als decimaal
1250    ← Geen scheidingsteken
up      ← Kleine letters
```

### ❌ Fout:
```
3,8     ← Komma werkt niet
1.250   ← Punt als duizendtal werkt niet
Up      ← Hoofdletter werkt niet
```

---

## 📤 CSV exporteren vanuit Excel

### Windows:
1. Bestand → Opslaan als
2. Bladeren naar gewenste map
3. Opslaan als type: **CSV UTF-8 (door komma's gescheiden) (*.csv)**
4. Opslaan

### Mac:
1. Bestand → Exporteren
2. Bestandsindeling: **CSV UTF-8 (.csv)**
3. Exporteren

---

## 🔧 Problemen oplossen

### "Geen geldige KPI data gevonden"
- Controleer of de eerste rij de headers bevat: `id,name,description,...`
- Controleer of er geen lege regels tussen de data staan

### Waarden worden niet correct weergegeven
- Controleer decimaalteken (punt, geen komma)
- Controleer of `type` correct is ingesteld

### CSV wordt niet herkend
- Zorg dat het bestand eindigt op `.csv`
- Probeer opnieuw te exporteren als "CSV UTF-8"

---

## 💡 Tips

1. **Backup**: Bewaar elke maand een kopie van je Excel (`kpi-jan-2026.xlsx`, etc.)
2. **Printen**: Ctrl+P (of Cmd+P) in de browser voor een printversie
3. **Presenteren**: F11 voor volledig scherm
4. **Download template**: In het dashboard kun je altijd een nieuwe template downloaden

---

## 📅 Maandelijkse checklist

- [ ] Open Excel template
- [ ] Update kolom E (currentValue) voor alle 8 KPI's
- [ ] Update kolom I (trend) waar nodig
- [ ] Exporteer als CSV
- [ ] Open dashboard en sleep CSV erin
- [ ] Controleer of alle waarden kloppen
- [ ] Maak backup van Excel-bestand

---

## 📞 Hulp nodig?

Neem contact op met IT (Rick) voor technische ondersteuning.

---

*Versie 3.0 | Januari 2026 | GMP+ International*
