# Oracle Fusion 1099 Reporting

## 1099 suppliers requirements

* Suppliers defined in Oracle need to have the following fields populated for 1099 reporting:
* Taxpayer ID
* Federal Reportable box must be selected
* Federal Income Tax Type (to determine which box on the 1099 the amount goes) Tax Reporting Name (OPTIONAL alternate name to use for the supplier on the 1099) Income Tax Region checked on one site for the supplier (usually the headquarters)

## Reporting Entities setup

Tax reporting entities must be created in **Setup and Maintenance -> Manage Reporting Entities**. For each reporting entity, assign Business Units and at least one balancing segment.

## 1099 patches from Oracle
Ensure that annual 1099 patches from Oracle have been applied. These are usually applied in November or early December for Fusion Cloud customers.

## 1099 exceptions reports

Run the following two reports (in Scheduled Processes) for each Business Unit/Reporting Entity combination:

* US 1099 Supplier Exceptions Report US 
* 1099 Invoice Exceptions Report
The Supplier Exceptions Report looks for errors or missing information in the following fields in supplier records: Taxpayer ID, Tax Reporting Site, State, Address, foreign supplier marked as Federal Reportable

The Invoice Exceptions Report looks for Federal Reportable suppliers with missing Income Tax Type, non-Federal Reportable suppliers with an Income Tax Type listed, and other errors on AP invoice lines.

## Correct errors found on exceptions reports
Update individual supplier records, or use the Suppliers Import spreadsheet to correct supplier records in mass.

## Update and Report Income Tax Details process

After completing supplier record updates, run the following Scheduled Process: Update and Report Income Tax Details. Run this for each Business Unit that has suppliers with records updated.

Run the exceptions reports again to verify records have been updated and no exceptions remain.

## US 1099 Payments Report

This Scheduled Processes report lists payments made to 1099 suppliers. Use this report to validate that each Federal Reportable supplier receives a 1099 with accurate totals.

Run this report for each reporting entity.

## US 1099 Report

This Scheduled Processes report prints all 1099s. Run for each reporting entity.

## US 1099 Electronic Media Report

This Scheduled Processes report outputs the electronic file to be transmitted to the IRS. Run for each reporting entity.
