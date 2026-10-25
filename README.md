# FinTech Data Quality — 50 Excel Records

## Overview

This beginner-level portfolio project demonstrates **data cleaning, validation, and data quality documentation** using 50 fictional payment and financial product records in Microsoft Excel.

The goal is to identify inconsistencies, apply basic data quality checks, and document cases that require clarification **without inventing or replacing missing amounts**.

> **Privacy note:** All records are fictional and intended solely for learning and portfolio demonstration. They do not represent real customers or transactions.

## Tools and Excel Functions

- **Microsoft Excel** for organizing, cleaning, and reviewing records.
- **ESPACIOS** (TRIM) to remove extra spaces from text.
- **SI** (IF) and **O** (OR) for validation rules.
- **CONTAR.SI** (COUNTIF) for summary indicators.
- Manual quality checks and findings documentation.

*Excel function names above are shown in Spanish because that is the language used in the original workbook.*

## Workbook Structure

The file `FinTech_Calidad_Datos_50_Portafolio.xlsx` contains six worksheets. Their original Spanish names are retained here so readers can find them in the workbook.

| Worksheet | Purpose |
| --- | --- |
| `Instrucciones` | Exercise goals, steps, and formula references. |
| `Resumen` | Data quality indicators and result checks. |
| `Pagos_50_Original` | Reference version containing formulas and earlier checks; these should not be mistaken for the final validation. |
| `Pagos_50_Limpio` | Main working sheet with text cleaning, validation rules, and record-level checks. |
| `Hallazgos` | Documentation of five amount-related issues and recommended actions. |
| `Solución` | References and examples of formulas used. |

## Workflow

1. Review the input fields and create cleaned-text columns using `ESPACIOS`.
2. Validate payment status against four allowed Spanish values: **Aprobada (Approved), Pendiente (Pending), Rechazada (Rejected), and Cancelada (Cancelled)**.
3. Flag missing or zero amounts as **Revisar (Review)**.
4. Check each record using the quality and verification columns.
5. Summarize the results using `CONTAR.SI` and document items requiring follow-up.

**Cleaning scope:** `ESPACIOS` removes extra spaces but does not independently standardize letter case. Status checks follow the rules documented in the workbook.

## Results

| Metric | Result |
| --- | ---: |
| Records reviewed | 50 |
| Valid status values | 50 |
| Status values requiring review | 0 |
| Valid amounts | 45 |
| Amounts requiring review | 5 |
| Payments with status `Cancelada` | 6 |

### Amount-Related Findings

**Five records require clarification:**

| Row in `Pagos_50_Limpio` | Finding | Recommended action |
| --- | --- | --- |
| 9 | Amount is $0.00 | Confirm whether zero is valid for this transaction. |
| 18 | Missing amount | Request the amount or confirm that it should remain blank. |
| 30 | Missing amount | Request the amount or confirm that it should remain blank. |
| 42 | Missing amount | Request the amount or confirm that it should remain blank. |
| 49 | Amount is $0.00 | Confirm whether zero is valid for this transaction. |

**Handling rule:** Suspicious amounts were flagged for review, not replaced with assumed values.

## Skills Demonstrated

- Basic Excel text cleaning and validation formulas.
- Detection of missing values and zero amounts.
- Quantitative data quality summaries.
- Structured documentation of findings and suggested next steps.
- Separation of reference data, working data, and supporting documentation.

## Limitations and Potential Improvements

This is an **introductory practice project**, not a financial audit or a production-ready automated system.

The `Pagos_50_Original` worksheet includes checks from an earlier stage. For the final results, refer to `Pagos_50_Limpio`, `Resumen`, and `Hallazgos`.

Potential improvements include explicit text-case normalization, additional validation rules, and a reproducible Power Query workflow.

## How to Review the Project

1. Download and open `FinTech_Calidad_Datos_50_Portafolio.xlsx` in Microsoft Excel.
2. Read `Instrucciones` for the exercise goals and rules.
3. Inspect `Pagos_50_Limpio` for cleaned records and validation checks.
4. Review `Resumen` for metrics and `Hallazgos` for the five flagged records.
5. Consult `Solución` for formula examples.

---

*Personal learning and portfolio project — Excel data cleaning and data quality.*
