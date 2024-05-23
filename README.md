QuickBase Automations
This repository contains scripts to automate various tasks related to QuickBase records. It includes a Bash script for querying and updating records, and a Python script for generating Excel reports and sending email notifications.

Contents
query_and_update.sh
generate_report.py

Prerequisites
Bash
cURL
Python 3
requests
openpyxl
smtplib

query_and_update.sh
This Bash script is designed to query QuickBase records, process the response, and update records based on specific criteria.

Setup
Replace the placeholder values for QUICKBASE_REALM, QUICKBASE_USR_TOKEN, QUICKBASE_DBID, and QUICKBASE_QUERY with actual data.

Ensure the script has execute permissions:
chmod +x query_and_update.sh

Usage
./query_and_update.sh

Script Details
Sets up variables for QuickBase API requests.
Constructs headers and JSON payloads for the API requests.
Queries records from QuickBase and processes the response.
Performs calculations and updates records based on specific conditions.
Handles records in different states and updates them accordingly.

generate_report.py
This Python script generates Excel reports from QuickBase records and sends email notifications with the generated reports as attachments.

Setup
Install the required Python packages:
pip install requests openpyxl

Replace the placeholder values for QUICKBASE_REALM, QUICKBASE_USR_TOKEN, QUICKBASE_DBID, and QUICKBASE_WO_QUERY with actual data.
Configure the email settings in the script.

Usage
python generate_report.py

Script Details
Calculates the date for the previous Sunday and formats it.
Queries QuickBase records using the QuickBase API.
Generates an Excel report with the queried data.
Styles the Excel report with custom fonts, colors, and merged cells.
Sends an email with the generated report as an attachment.
