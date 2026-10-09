# HR Analytics Dashboard — Power BI
<img width="1639" height="960" alt="ChatGPT Image Oct 9, 2026, 09_45_09 PM" src="https://github.com/user-attachments/assets/9f18af3b-7922-4d35-bf61-aeda79cf88fd" />



An interactive HR analytics report built in Microsoft Power BI. The report brings together employee overview, demographics, performance tracking, and attrition analysis in one navigable dashboard.

## Dashboard pages

The PBIX report contains four report pages:

| Page | What it covers |
| --- | --- |
| **Overview** | Total and active employees, active employees by department and job role, and employee totals by year and attrition status. |
| **Demographics** | Employee breakdowns by marital status and ethnicity, average salary by ethnicity, and age/gender exploration. |
| **Performance Tracker** | Rating and satisfaction indicators, review dates, and yearly trends for environment, job, manager, relationship, self, and work-life balance. |
| **Attrition** | Attrition rate by department, years at company, business travel, overtime, and year. The source page is named `Atrrition` inside the PBIX. |

The report includes interactive slicers for year, gender, department, and—on the Performance Tracker page—employee name.

## Data model observed in the report

The model layout embedded in the PBIX lists the following tables:

- `FactPerformanceRating`
- `DimEmployee`
- `DimEducationLevel`
- `DimRatingLevel`
- `DimSatisfiedLevel`
- `DimDate`
- `_Measures`
- `Table`

The report visuals reference employee attributes such as department, job role, gender, age, age bins, ethnicity, salary, marital status, business travel, overtime, years at company, attrition, full name, and hire date.

Referenced measures include total employees, active employees, attrition rate, total employee date, review dates, and performance dimensions.

See the [observed data dictionary](docs/data-dictionary.md) for the field-level inventory.

## Visual design

- Dark navy report background (`#111A26`).
- Custom `Charcoal_and_Lime` theme included in `assets/charcoal-and-lime-theme.json`.
- Embedded Atlas Lab logo and employee avatar assets are included under `assets/`.

## Files

```text
.
├── atlas.pbix
├── README.md
├── .gitignore
├── assets/
│   ├── atlas-lab-logo.png
│   ├── charcoal-and-lime-theme.json
│   ├── employee-avatar-female.png
│   └── employee-avatar-male.png
└── docs/
    ├── data-dictionary.md
    ├── github-upload.md
    ├── linkedin-post.md
    └── verification-notes.md
```

## How to open the report

1. Install or open Microsoft Power BI Desktop.
2. Open `atlas.pbix`.
3. Use the page navigator and slicers to explore the report.

GitHub stores the PBIX and its documentation; it does not render the interactive Power BI report in the repository page. Anyone reviewing the project will need Power BI Desktop to open the PBIX.

## Publishing checklist

Before making the repository public, confirm that the PBIX contains only data and assets you are allowed to publish.

Also confirm that no connection files, credentials, or local paths are committed.

The included PBIX is approximately 0.88 MiB, so it is small enough for a normal GitHub upload.
