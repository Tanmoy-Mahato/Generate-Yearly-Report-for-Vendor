# Generate Yearly Report – UiPath RPA Automation

## Overview

This UiPath automation generates yearly vendor reports by downloading all monthly reports for a vendor from ACME System 1, merging them into a single Excel file, and uploading the final yearly report back into the system.

The bot processes WI4 work items automatically and updates each transaction with the generated Upload ID.

---

## Process Details

| Item | Details |
|------|----------|
| Process Name | Generate Yearly Report for Vendor |
| Department | Finance and Accounting |
| Function | Reporting |
| Schedule | Yearly (Mid-January) |
| Average Volume | 7–15 Vendors |
| Average Handling Time | ~15 min/vendor |
| Robot Type | Back Office Robot |
| Automation Scope | 100% Automated |

---

## Workflow Steps

| Step | Description |
|------|-------------|
| 1.1 | Open ACME System 1 Web Application |
| 1.2 | Log in using email and password |
| 1.3 | Access Dashboard |
| 1.4 | Open Work Items listing |
| 1.5 | Process each WI4 activity |
| 1.5.A | Retrieve Vendor Tax ID from Work Item Details |
| 1.5.B | Open Download Monthly Report section |
| 1.5.C | Download all monthly reports for 2025 |
| 1.5.D | Merge reports into yearly Excel report |
| 1.5.E | Open Upload Yearly Report section |
| 1.5.F | Upload yearly report and retrieve Upload ID |
| 1.5.G | Open Update Work Item page |
| 1.5.H | Mark item as Completed and add Upload ID in comments |
| 1.6 | Continue with next WI4 activity |

---

## Report Naming Convention

```text
Yearly-Report-2025-TAXID.xlsx
```

---

## Input Data

The bot uses:

- Vendor Tax ID
- Monthly Vendor Reports

---

## Output

The automation generates:

- Consolidated Yearly Excel Report
- Upload ID after successful upload

Example comment added to Work Item:

```text
Uploaded with ID [uploadID]
```

---

## Technologies Used

- UiPath Studio
- UiPath Orchestrator
- ACME System 1
- Microsoft Excel
- Web Automation

---

## Security & Credential Management

Credentials are securely stored using:

- UiPath Orchestrator Assets

No credentials are hardcoded inside workflows.

---

## Project Structure

```text
Project
│
├── Main.xaml
├── Framework/
├── Workflows/
├── Config/
├── Data/
├── Reports/
├── Assets/
└── README.md
```
