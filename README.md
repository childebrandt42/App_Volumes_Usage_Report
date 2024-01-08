<p align="center">
    <a href="https://twitter.com/childebrandt42" alt="Twitter">
            <img src="https://img.shields.io/twitter/follow/Childebrandt42.svg?style=social"/></a>
</p>
<!-- ********** DO NOT EDIT THESE LINKS ********** -->

# VMware App Volumes Usage Report

VMware App Volumes Usage report which works in conjunction with [ImportExcel Powershell Module](https://github.com/dfinke/ImportExcel).

Please refer to my blog [Blog Website](https://www.childebrandt42.blog) for more detailed information about this project. 

Blog post for this project [Blog Post](https://childebrandt42.blog/2024/02/13/app-volumes-usage-report-decoding-the-signals-for-retiring-old-applications-with-precision)

# :books: Sample Reports

## Sample Report
Sample App Volumes Writable Usage Report CSV: [Sample-PackageReport-CSV.csv](https://htmlpreview.github.io/?https://github.com/childebrandt42/App_Volumes_Usage_Report/main/Samples/Sample-PackageReport-CSV.csv)

Sample App Volumes User Usage Report CSV: [Sample-UserReport-CSV.csv](https://htmlpreview.github.io/?https://github.com/childebrandt42/App_Volumes_Usage_Report/main/Samples/Sample-UserReport-CSV.csv)

Sample App Volumes Writable Usage Report CSV: [Sample-WritableReport-CSV.csv](https://htmlpreview.github.io/?https://github.com/childebrandt42/App_Volumes_Usage_Report/main/Samples/Sample-WritableReport-CSV.csv)


Sample App Volumes Usage Report Excel format: [Sample-AppVolumesUsageReport-Excel.xlsx](https://htmlpreview.github.io/?https://github.com/childebrandt42/App_Volumes_Usage_Report/main/Samples/Sample-AppVolumesUsageReport-Excel.xlsx)

# :beginner: Getting Started
Below are the instructions on how to run the VMware Horizon Usage Report

### PowerShell
This report is compatible with the following PowerShell versions;

<!-- ********** Update supported PowerShell versions ********** -->
| Windows PowerShell 5.1 |     PowerShell 7    |
|:----------------------:|:--------------------:|
|   :white_check_mark:   | :white_check_mark: |
## :wrench: System Requirements
<!-- ********** Update system requirements ********** -->
PowerShell 5.1 or PowerShell 7, and the following PowerShell modules are required for generating a VMware Horizon Usage Report.

- [Import Excel Module](https://www.powershellgallery.com/packages/ImportExcel/)

## :package: Instructions

Download script

Fill in the Varribles
$AppVolServer = AppVolumes Server FQDN
$Creds = Enter your Creds for App Volumes server
$ReportLocation = Report Save Location
$ReportName = Report name if in Excel Format
$ReportType = Report type
$UserReportName = User Report Name if CSV format is used
$PackageReportName = Package Report Name if CSV format is used
$WritableReportName = Writable Report Name if CSV format is used

Report will work in both CSV or Excel exports, If you choose CSV it will create 3 seperate files, and Excel will create 1 Excel with 3 workbooks.

This report will generate User Usage Reports, Package Usage Report, and also Writable Usage Report.

User Usage Report:
User Name | Total Logins | Last Login Date
----------|--------------|-------------------
CHRISLAB\Administrator | 30 | Nov 17 2023 02:01PM
CHRISLAB\Chris | 34 | Dec 10 2023 11:20AM
CHRISLAB\Test2 | 336 | Jan 02 2024 08:23PM
CHRISLAB\Test3 | 333 | Jan 02 2024 06:23PM
CHRISLAB\Test4 | 333 | Jan 02 2024 06:53PM
CHRISLAB\Test5 | 332 | Jan 02 2024 07:53PM

Package Usage Report:
Package Name | Stage | Current State | Total Usage | Last Used
-------------|-------|---------------|-------------|----------
Adobe Reader 2.0.0.720 | Published | Current | 2 | 2023-11-17
Prusa Slicer 2.6.1 | Published | Current | 2 | 2023-11-17
Chrome 1.3.36.312 | Published | Current | 1 | 2023-11-17
Firefox 18.5 | Published | Current | 1 | 2023-11-17
Notepad++ 8.5.8 | Published | Current | 3 | 2023-11-17
Zoom 5.16.0 | Published | Current | 175 | 2024-01-03
WinSCP 6.1.2 | Published | Current | 1 | 2023-11-17
VLC 3.0.30 | Published | Current | 2 | 2023-11-17
Open Office 4.1.1.4 | Published | Current | 1 | 2023-11-17
GreenShot 1.2.10.6 | Published | Current | 1 | 2023-11-17
Putty 0.79 | Published | Current | 1 | 2023-11-17
7Zip 2301 | Published | Current | 1 | 2023-11-17
Blender 4.0.1 | Published | Current | 1 | 2023-11-17
Wireshark 4.2.0 | Published | Current | 1 | 2023-11-17
Office 365, Teams, OneDrive | Published | Current | 510 | 2024-01-03
Office 365, Teams, OneDrive-update | New | Not Current | 0 | Never

Writable Usage Report:
Writable Name | Owner Name | Num of Times Mounted | Date Last Mounted
--------------|------------|----------------------|------------------
CHRISLAB\Chris | Chris | 0	
CHRISLAB\Test19 | Test19 | 0	