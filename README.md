# balance_study

The idea is to transform a time consuming, mundane Excel report into a quick, easy to use report in Python.

Note: This project is a small part of a larger project.  The complete project is the Employee Balance and Payroll Calculator.  The complete project will use:

* Input from this *balance_study* project
* Input from *donations*
* Input from *expenses*
* All linked together with *gl_codes*
* Salary report exported from payroll software
* Budgeted payroll spreadsheet

## Current situation

* A financial report (spreadsheet with one-tab per employee) is emailed to Ops Manager around the 10th of each month. This report has closing balance information for each employee.
* The balance information is transcribed into a *current balance* spreadsheet
* The *current balance* spreadsheet receives the following manual input:
    *  balance
    *  donations
    *  expenses
    *  name
    *  actual working balance (the target)
*  The *actual working balance* is entered into the _**Approved Payroll Sheet**_ (ultimate goal)

## Proposed solution (for now)

* Use Python with *Openpyxl, Pandas, etc.* to extract employee name and ending balance from the monthly financial report
* Run a monthly donation report and save it as a csv file
* Keep a running tab of expense reimbursements via a simple csv file
* Calculate admin assessment from monthly donations
* Use a *gl code* csv as a dictionary to keep track of employee name, id, gl code, ministry name -- naming conventions
* Use ending balance + (donations-assessment) - expenses = current balance

## The balance_study part

* Use Python with *Openpyxl, Pandas, etc.* to extract employee name and ending balance from the monthly financial report
* Current problem: Figuring out how to loop through sheets and extract *name* (kind of figured out) and *ending balance*
* This is the most confusing of all of the other parts.

### Desired output

![output](https://user-images.githubusercontent.com/39529379/110819361-58dd7a80-824b-11eb-888c-7457d186e6dc.png)

