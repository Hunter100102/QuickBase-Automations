# QuickBase Automations

This repository contains scripts to automate various tasks related to QuickBase records. It includes a Bash script for querying and updating records, and a Python script for generating Excel reports and sending email notifications.

## Contents
- `Po_invoice_creater.sh`
- `Excel File Builder.py`

## Prerequisites
- **Bash**
- **cURL**
- **Python 3**
  - `requests`
  - `openpyxl`
  - `smtplib`

## Scripts Overview

### `query_and_update.sh`

This Bash script is designed to query QuickBase records, process the response, and update records based on specific criteria.

#### Setup
1. Replace the placeholder values for `QUICKBASE_REALM`, `QUICKBASE_USR_TOKEN`, `QUICKBASE_DBID`, and `QUICKBASE_QUERY` with actual data.
2. Ensure the script has execute permissions:
   ```bash
   chmod +x query_and_update.sh
   ```

#### Usage
To run the script, use:
```bash
./query_and_update.sh
```

#### Script Details
- **Setup Variables:** Initializes variables for QuickBase API requests.
- **Construct Requests:** Constructs headers and JSON payloads for the API requests.
- **Query Records:** Queries records from QuickBase and processes the response.
- **Update Records:** Performs calculations and updates records based on specific conditions.
- **Handle States:** Manages records in different states and updates them accordingly.

### `generate_report.py`

This Python script generates Excel reports from QuickBase records and sends email notifications with the generated reports as attachments.

#### Setup
1. Install the required Python packages:
   ```bash
   pip install requests openpyxl
   ```
2. Replace the placeholder values for `QUICKBASE_REALM`, `QUICKBASE_USR_TOKEN`, `QUICKBASE_DBID`, and `QUICKBASE_WO_QUERY` with actual data.
3. Configure the email settings in the script.

#### Usage
To run the script, use:
```bash
python generate_report.py
```

#### Script Details
- **Date Calculation:** Calculates the date for the previous Sunday and formats it.
- **Query Records:** Queries QuickBase records using the QuickBase API.
- **Generate Report:** Creates an Excel report with the queried data.
- **Style Report:** Styles the Excel report with custom fonts, colors, and merged cells.
- **Send Email:** Sends an email with the generated report as an attachment.

---
