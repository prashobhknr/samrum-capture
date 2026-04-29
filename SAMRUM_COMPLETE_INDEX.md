# SAMRUM Application Capture Index

## Overview
Complete capture of the SAMRUM ASP.NET WebForms application for AI reimplementation.
- **Site:** http://app.samrum.se/
- **Total pages captured:** ~472 pages
- **Capture date:** 2026-04-29
- **Technology:** ASP.NET WebForms (Visual Basic .NET)

## File Structure

### Markdown Documentation
- `SAMRUM_PhaseA_B2_spec.md` - Structural specification (Phases A + B2, ~95 pages)
- `SAMRUM_COMPLETE_INDEX.md` - This file

### JSON Data Files
- `SAMRUM_captures_A_B2.json` - Phase A + B2 captures (95 pages, ~4.66 MB)
- `SAMRUM_PhaseC_part1_captures.json` - Phase C pages C_001–C_100 (100 pages)
- `SAMRUM_PhaseC_part2_captures.json` - Phase C pages C_101–C_150 (50 pages)
- `SAMRUM_PhaseC_part3_captures.json` - Phase C pages C_151–C_200 (50 pages)
- `SAMRUM_PhaseC_part4_captures.json` - Phase C pages C_201–C_250 (50 pages)
- `SAMRUM_PhaseC_part5_captures.json` - Phase C pages C_251–C_300 (50 pages)
- `SAMRUM_PhaseC_part6_captures.json` - Phase C pages C_301–C_350 (50 pages)
- `SAMRUM_PhaseC_part7_FINAL_captures.json` - Phase C pages C_351–C_372 (22 pages)

## Phase Descriptions

### Phase A (Baseline, 48 pages)
Structural sample — one representative per module, all top-nav pages, DBA root, forms.

### Phase B2 (Targeted, 47 pages)
2-3 PMO leaves per module + DBA detail pages + object detail forms + user admin pages.

### Phase C (Full Crawl, 372 pages)
ALL remaining PMO leaf nodes — complete coverage of all project module pages.

## URL Patterns
| Page Type | URL Pattern |
|-----------|-------------|
| Module page | `modulePage.aspx?ProjectModuleId=NNN` |
| Object detail | `main.aspx?ObjectInstanceId=NNN&ProjectModuleId=NNN&DisplayMode=1` |
| Object create | `main.aspx?ObjectTypeId=NNN&ProjectModuleId=NNN&DisplayMode=2` |
| DBA | `DatabaseAdministration.aspx` |
| User admin | `UserAdministrationPage.aspx?UserId=NNN` |
| View designer | `ReportViewEditor.aspx?ProjectModuleId=NNN` |
| Help | `Help/hh_start.htm` |

## JSON Data Format
Each JSON file contains an array of captured page objects:
```json
{
  "name": "C_001_BRF_Tekniska_system_PMO1540",
  "url": "http://app.samrum.se/modulePage.aspx?ProjectModuleId=1540",
  "capturedAt": "2026-04-28T...",
  "html": "...(truncated at 100,000 chars)...",
  "labels": ["Label text 1", "Label text 2", ...],
  "inputs": [
    {"type": "text", "name": "fieldName", "id": "...", "value": "...", "label": "..."},
    ...
  ],
  "buttons": [
    {"text": "Button text", "href": "...", "type": "..."},
    ...
  ]
}
```

## All PMO Module IDs (413 leaves total)
Captured from the navigation tree. Phase A+B2 covered IDs including:
136, 271, 1538, 1539, 341, 340, 94, 67, 204, 205, 114, 96, 198, 148, 192, 195, 
68, 373, 243, 183, 85, 161, 158, 93, 267, 233, 232, 236, 176, 175, 133, 365, 366, 
265, 234, 235, 238, 249, 193, 200 (and more in Phase B2)

Phase C captured all remaining 372 IDs automatically.
