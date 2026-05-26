# Automation & QA Developer - Skills Assessment Submission

This repository contains the deliverables for the Automation & QA Developer take-home assessment.

## Project Overview

### Task 1: Web App QA & Debug Report
- **Target Application:** Conduit (RealWorld Live Demo - https://demo.realworld.io)
- **Objective:** Evaluated core user flows to identify major functional, UX, and security issues.
- **Deliverable:** Included in this repo as `Task1_QA_Report.pdf`.

### Task 2: n8n API Integration Workflow
- **Objective:** Built an automated morning brief pipeline that dynamically fetches and processes data without hardcoded secrets.
- **APIs Used:** GitHub REST API.
- **Transformation Logic:** A JavaScript Code node reduces the primary payload down to the top 5 trending JavaScript repositories. The workflow then grabs detailed metadata for the top item.
- **Conditional Branching:** Evaluates if the top repository has a star count exceeding 5,000. 
- **Error Handling:** Configured to "Continue On Fail" across HTTP endpoints. API errors are wrapped into an error object and passed downstream, ensuring the system never crashes silently.
- **Deliverable:** Exported as `Task2_Workflow.json`.

### Bonus Task: Uptime Monitor
- **Objective:** A standalone n8n workflow scheduled to ping the target web application every 5 minutes. It checks for a `200 OK` status and routes downtime alerts to a notification channel if a failure occurs.
- **Deliverable:** Exported as `Bonus_UptimeMonitor.json`.
