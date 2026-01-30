# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

GMP+ International OGSM 2026-2028 KPI Dashboard - a standalone HTML application for monitoring 8 strategic KPIs. Built with vanilla HTML/CSS/JavaScript with zero dependencies.

## Development

**No build system required.** Open `index.html` directly in any browser.

- All code is in a single file: `index.html`
- Works completely offline
- No package manager, bundler, or compilation step

## Architecture

The application is a single HTML file with three sections:

1. **CSS (lines ~7-446)**: GMP+ branded styling with CSS variables, responsive grid layout, print media queries
2. **HTML (lines ~448-505)**: Dashboard structure with drag-drop upload area, KPI grid container, legend
3. **JavaScript (lines ~507-876)**: CSV parsing, data processing, SVG donut chart rendering

### Data Flow

1. User uploads CSV via drag-and-drop or file picker
2. `parseCSV()` handles both comma and semicolon delimiters, quoted fields
3. `processCSVToKPIs()` converts rows to KPI objects with validation
4. `renderDashboard()` creates donut chart cards using inline SVG

### KPI Data Model

CSV columns: `id`, `name`, `description`, `category`, `currentValue`, `targetValue`, `unit`, `type`, `trend`

Types: `percentage`, `rating`, `number`
Trends: `up`, `down`, `stable`

### Color Logic

Status colors are calculated by achievement percentage (currentValue/targetValue):
- Green: >= 80%
- Orange: 50-80%
- Red: < 50%

## Localization

All UI text is in Dutch (Netherlands). Key terms:
- "Laatst bijgewerkt" = Last updated
- "Huidige waarde" = Current value
- "Doel" = Target/Goal

## Supporting Files

- `kpi-data-template.xlsx` - Excel template for users to edit monthly data
- `kpi-data-template.csv` - Sample CSV for testing
- `INSTRUCTIES.md` - Dutch user instructions with workflow and troubleshooting
