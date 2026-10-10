# HR Analytics Dashboard (Excel)

![HR Analytics dashboard](HR%20Dashboard.png)

An interactive Excel dashboard that tracks headcount, attrition, diversity, job levels, tenure and manager workload for a 171-employee dataset covering 2020 to 2025. HR leaders can filter by department, manager and other fields to see where workforce risk sits.

**Tools:** Excel (Power Query, PivotTables, PivotCharts, slicers)
**Domain:** Human resources analytics, workforce planning

---

## Business problem

HR leaders often rely on one overall attrition number, which hides where people are actually leaving. This dashboard breaks workforce data down by department, job level, tenure and reporting manager, so retention, hiring and manager-load decisions can target specific groups.

## Questions the dashboard answers

1. How many employees are active, how many have left, and how many moved internally?
2. How has headcount changed from 2020 to 2025?
3. What is the gender mix, and how does it look by job level?
4. Which departments hold the most employees?
5. How is the workforce spread across job levels (Trainee, Professional, Management, Contract)?
6. How many people report to each manager?
7. How long do employees stay?

## Dataset

- **Source:** HR raw dataset (a practice dataset, included as `HR Raw Dataset.xlsb`)
- **Size:** 171 employee records, 2020 to 2025
- **Main fields:** department, job level, gender, reporting manager, joining date, exit date or status, tenure
- **Privacy:** this is a sample dataset with no real employee data.

## Approach

1. **Clean** the raw data in Power Query: fix data types, handle blanks, standardize labels, create tenure bands.
2. **Define the metrics** (see below) so each number has one clear meaning.
3. **Analyze** with PivotTables for headcount, attrition, diversity, job level, tenure and manager spans.
4. **Visualize** with PivotCharts and KPI cards on one dashboard sheet, with slicers for drill-down.

## Metric definitions

| Metric | Definition |
|---|---|
| Total employees | All records in the dataset (171) |
| Active headcount | Employees still with the company (118) |
| Attrition | Employees who left (47) |
| Attrition rate | Attrition ÷ total employees = 47 ÷ 171 = 27% |
| Internal transfers | Employees who moved within the company (6) |

The 27% attrition rate covers the whole 2020 to 2025 period. It is a cumulative figure, not an annual rate, so it should not be compared directly with industry annual attrition benchmarks.

## Key findings

| Area | Finding |
|---|---|
| Workforce | 171 employees: 118 active, 47 left, 6 transferred |
| Attrition | 27% of all employees in the dataset have left |
| Gender mix | 62% male, 38% female |
| Department concentration | Operations and Sales hold the largest headcount |
| Tenure | Most employees sit in two groups: 2 years or less, and 5 years or more |
| Manager spans | Number of direct reports varies noticeably between managers |

Read these as patterns in the sample data, not as proven causes.

## Recommendations

These are hypotheses for an HR team to test, based on what the dashboard shows.

1. **Check retention in Operations and Sales first.** They hold the most people, so each exit there affects the business most. Compare their attrition rate with other departments before acting.
2. **Review the first two years.** A large group sits in the 2-years-or-less tenure band. Look at whether onboarding and early-career support can improve retention.
3. **Set a target span of control.** Manager team sizes vary. Define an acceptable range and flag managers outside it.
4. **Look at gender mix by job level.** The overall 62/38 split says little until you see whether women are under-represented in management specifically.
5. **Add an annual attrition rate.** This makes the numbers comparable with benchmarks and shows whether attrition is rising or falling.

## Limitations

- With only 171 employees, department and manager figures rest on small groups, so one or two exits can swing a percentage.
- The dataset has no exit reasons, salary, performance or engagement data, so I can show where people leave but not why.
- The gender field shows a 62/38 split but does not prove bias in hiring or promotion.
- The attrition rate is cumulative across the period, as explained above.

## Next steps

- Add annual attrition rate by year, department and job level.
- Add tenure-at-exit analysis to see when people tend to leave.
- Add exit-reason data if available.
- Rebuild the dashboard in Power BI and compare it with this Excel version.

## Repository contents

```
├── HR Raw Dataset.xlsb              # raw dataset
├── pivot + dashboard HR.xlsx        # PivotTables and dashboard
├── HR Dashboard.png                 # dashboard screenshot
├── HR analysis.pdf                  # exported report
└── README.md
```

**To explore:** download `pivot + dashboard HR.xlsx`, open it in Excel, and use the slicers on the dashboard sheet.

## Skills demonstrated

Data cleaning (Power Query) · PivotTables and PivotCharts · KPI and metric definition · Dashboard design with slicers · HR and workforce analysis · Turning findings into recommendations

## Author

**Bharat Sinha**, aspiring data analyst
[LinkedIn](https://www.linkedin.com/in/bharat-sinha-122791130/) | [GitHub](https://github.com/bharat-sinha) | sinha.bharat8@gmail.com
