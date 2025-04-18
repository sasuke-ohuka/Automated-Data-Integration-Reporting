# Automated-Data-Integration-Reporting
This project consolidates data from various departments and platforms into a unified reporting system.
# Data Integration & Workflow Automation

Automating the process of syncing departmental spreadsheets into a central SQL database.

## Goal
- Eliminate manual entry
- Ensure consistent and real-time data flow
- Reduce human error

## Tools
- Google Sheets API
- SQL Server
- Excel Macros (VBA)

## Features
- Fetches new data weekly via script
- Runs integrity checks before database insertion
- Logs sync activity for auditing

## SQL Sample
```sql
MERGE INTO central_db AS target
USING source_sheet AS src
ON target.user_id = src.user_id
WHEN MATCHED THEN UPDATE SET ...
WHEN NOT MATCHED THEN INSERT ...
