# Reliable Insight Agent

A healthcare analytics pipeline that investigates monthly KPI changes and generates reports for analysts and executives.

I developed this project during my summer 2026 internship with Ascension Data Science Institute’s Data Science & AI Center of Excellence, with guidance and feedback from my mentor.

## Example reports

Both examples use synthetic healthcare data. The organizations, financial figures, and operational changes are illustrative.

- [Executive brief](executive-example.html): A concise summary of KPI changes, potential business implications, and recommended follow-up.
- [Analyst report](analyst-example.html): Detailed findings, investigation steps, underlying evidence, open questions, and SQL provenance.

Download the HTML files and open them in a browser to explore the reports.

## How it works

1. Fetch KPI values from BigQuery.
2. Detect month-over-month changes using explicit Python rules.
3. Execute SQL investigation playbooks.
4. Use Gemini to interpret results and propose follow-up investigations.
5. Validate tool requests and check generated claims against query results.
6. Generate separate analyst and executive reports.

Python controls execution. Gemini provides interpretation and proposes additional investigation within defined limits.

## Technology

Python, SQL, Google BigQuery, Gemini, and Streamlit.

## Reliability and limitations

The pipeline includes numeric checks, semantic verification, query traceability, and explicit evidence gaps.

These checks support review; they do not guarantee that every interpretation is correct. In particular, numeric agreement does not establish causation, seasonality, or a persistent structural change. Some language in the example reports should be read as exploratory interpretation.

## Repository scope

This repository currently contains example outputs and a project overview. Source code is not included. A reviewed technical record will be added separately.
