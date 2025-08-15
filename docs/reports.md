---
layout: default
title: Reports - Worked Hours Report
description: Generate and export worked hours reports for employees and locations
---

# Reports - Worked Hours Report

The Worked Hours Report feature allows you to generate comprehensive reports showing employee working hours, holiday data, and location-based summaries. These reports can be exported in PDF or Excel formats for analysis, compliance, and record-keeping.

---

## 🎯 Overview

### What the Worked Hours Report Provides

- **Employee-specific reports**: Detailed breakdown of hours worked by individual employees
- **Location-based reports**: Summary of all employees' hours within a specific location
- **Holiday integration**: Automatic inclusion of approved holiday periods
- **Flexible date ranges**: Predefined periods or custom date ranges
- **Multiple export formats**: PDF for presentation, Excel for data analysis

### Key Features

- ✅ **Multi-tenant support**: Reports are scoped to your company
- ✅ **Role-based access**: Only users with `reports.read` permission can access
- ✅ **Real-time data**: Reports reflect current shift assignments and holiday data
- ✅ **Holiday awareness**: Shows holiday periods and excludes them from worked hours
- ✅ **Export capabilities**: Download as PDF or Excel files

---

## 🚀 Getting Started

### Accessing Reports

1. **Navigate to Reports**

   - Click on "Reports" in the main sidebar navigation
   - You must have the `reports.read` permission to see this option

2. **Select Worked Hours Report**
   - From the reports landing page, click on "Worked Hours Report"
   - This opens the report builder interface

### Report Builder Interface

The report builder provides a user-friendly interface to configure your report:

```
┌─────────────────────────────────────────────────────────┐
│                    Worked Hours Report                  │
├─────────────────────────────────────────────────────────┤
│ Group By: ○ By Employee  ● By Location                 │
│                                                         │
│ Employee: [Select Employee ▼]                          │
│ Location: [Select Location ▼]                          │
│                                                         │
│ Date Range: ● Last 7 Days  ○ Last 30 Days              │
│            ○ Last 90 Days  ○ This Month                │
│            ○ Last Month   ○ This Quarter               │
│            ○ Custom Range                               │
│                                                         │
│ [Generate Preview]  [Download Excel]  [Download PDF]   │
└─────────────────────────────────────────────────────────┘
```

---

## 📊 Report Types

### 1. Employee Reports (By Employee)

**Purpose**: Detailed analysis of individual employee working patterns and holiday usage.

**What's Included**:

- Employee personal information
- Total worked hours for the period
- Holiday summary (taken days, working days)
- Detailed shift breakdown by date
- Holiday dates with descriptions
- Hour calculations excluding holiday periods

**Example Output**:

```
Employee: Ecaterina Pop (ecaterina.pop@yahoo.com)
Period: 01-08-2025 - 31-08-2025
Total Hours: 12.0h (1 holidays)

Holiday Summary: 1 Taken, 6 Working Days
Holiday dates: 11-08-2025 - 17-08-2025

Daily Breakdown:
- 01-08-2025: 8.0h (Morning Shift)
- 02-08-2025: 8.0h (Afternoon Shift)
- 11-08-2025: Holiday
- 12-08-2025: Holiday
- ...
```

### 2. Location Reports (By Location)

**Purpose**: Overview of all employees' working hours within a specific location.

**What's Included**:

- Location information
- Summary of all employees in the location
- Individual employee breakdowns
- Per-user shift and holiday details
- Total location hours
- Holiday details by employee

**Example Output**:

```
Location: Downtown Office
Period: 01-08-2025 - 31-08-2025

Employees:
- Alexandra Tot: 48.0h
- Emiliana Grigore: 48.0h
- Ion Popescu: 23.9h
- Ecaterina Pop: 12.0h (1 holidays)

Detailed Breakdown:
Alexandra Tot:
- 01-08-2025: 8.0h (Morning Shift)
- 02-08-2025: 8.0h (Afternoon Shift)
- ...

Ecaterina Pop:
- 01-08-2025: 8.0h (Morning Shift)
- 11-08-2025: Holiday
- ...
```

---

## 📅 Date Range Options

### Predefined Periods

| Option           | Description               | Use Case               |
| ---------------- | ------------------------- | ---------------------- |
| **Last 7 Days**  | Previous 7 calendar days  | Weekly reviews         |
| **Last 30 Days** | Previous 30 calendar days | Monthly summaries      |
| **Last 90 Days** | Previous 90 calendar days | Quarterly analysis     |
| **This Month**   | Current month to date     | Current month tracking |
| **Last Month**   | Complete previous month   | Monthly comparisons    |
| **This Quarter** | Current quarter to date   | Quarterly planning     |

### Custom Date Range

For more specific analysis, you can select custom dates:

1. **Select "Custom Range"**
2. **Choose Start Date**: Click the start date picker
3. **Choose End Date**: Click the end date picker
4. **Validation**: System ensures end date is after start date
5. **Maximum Range**: Limited to 365 days for performance

---

## 📋 Report Generation Process

### Step 1: Configure Report

1. **Select Grouping**

   - Choose "By Employee" for individual analysis
   - Choose "By Location" for team/location overview

2. **Select Target**

   - **For Employee reports**: Select specific employee from dropdown
   - **For Location reports**: Select specific location from dropdown

3. **Choose Date Range**
   - Select from predefined periods or custom range
   - Ensure dates are valid and within limits

### Step 2: Generate Preview

1. **Click "Generate Preview"**

   - System validates your selections
   - Shows any validation errors
   - Displays report data in the interface

2. **Review Data**
   - Check that the correct data is displayed
   - Verify date ranges and employee/location selections
   - Review holiday information accuracy

### Step 3: Export Report

1. **Choose Export Format**

   - **PDF**: For presentations, printing, and formal documentation
   - **Excel**: For data analysis, calculations, and further processing

2. **Download Report**
   - Click "Download Excel Report" or "Download PDF Report"
   - File downloads automatically to your device
   - Filename includes report type and date range

---

## 📄 Export Formats

### PDF Reports

**Best for**: Presentations, printing, formal documentation, compliance records

**Features**:

- Professional formatting with company branding
- Page breaks automatically managed
- Consistent layout across all reports
- Ready for printing or sharing

**Content Structure**:

- Header with company and report information
- Summary section with totals
- Detailed breakdown tables
- Footer with generation timestamp

### Excel Reports

**Best for**: Data analysis, calculations, further processing, integration with other systems

**Features**:

- Multiple worksheets for different data views
- Structured data for easy filtering and sorting
- Formulas for calculations
- Compatible with other analysis tools

**Worksheet Structure**:

- **Summary Sheet**: Overview of all data
- **User Detail Sheet**: Individual employee breakdowns
- **Location Detail Sheet**: Location-based summaries
- **Holiday Details**: Comprehensive holiday information

---

## 🔍 Understanding Report Data

### Worked Hours Calculation

**Formula**: `Total Hours = Sum of all shift hours - Holiday periods`

**Key Points**:

- Only includes shifts with `ACTIVE` status
- Holiday periods are excluded from worked hours
- Hours are calculated based on shift start/end times
- Overtime and special rates are not currently included

### Holiday Data Integration

**What's Included**:

- Approved holiday requests within the report period
- Holiday dates and descriptions
- Impact on total worked hours calculation

**What's Excluded**:

- Pending holiday requests
- Rejected holiday requests
- Holidays outside the report period

### Data Sources

**Primary Data**:

- `ShiftAssignment` table: Actual worked/scheduled shifts
- `HolidayRequest` table: Approved holiday periods
- `User` table: Employee information
- `Location` table: Location details

**Data Freshness**:

- Reports reflect real-time data
- No caching or delayed updates
- Always shows current state of assignments

---

## ⚠️ Important Notes

### Performance Considerations

- **Large Date Ranges**: Reports with very long periods may take longer to generate
- **Many Employees**: Location reports with many employees may be slower
- **Export Size**: Large reports may result in bigger file sizes

### Data Limitations

- **Historical Data**: Only includes data from when the system was implemented
- **Deleted Records**: Permanently deleted shifts/holidays are not included
- **Archived Data**: Data older than 6 months may be archived (if retention policies are enabled)

### Access Control

- **Permission Required**: `reports.read` permission is mandatory
- **Company Scope**: Users can only access reports for their company
- **Data Privacy**: Reports respect user privacy and data protection settings

---

## 🛠️ Troubleshooting

### Common Issues

**"No Data Found" Message**

- Check that the selected date range contains data
- Verify the employee/location has active assignments
- Ensure the user has the correct permissions

**Empty Dropdowns**

- Refresh the page to reload employee/location data
- Check that users and locations exist in the system
- Verify your company context is properly set

**Export Failures**

- Check your internet connection
- Ensure you have sufficient disk space
- Try generating a smaller date range

**Permission Errors**

- Contact your administrator to grant `reports.read` permission
- Verify you're logged into the correct company account
- Check that your user account is active

### Getting Help

If you encounter issues:

1. **Check the troubleshooting section above**
2. **Verify your permissions and company context**
3. **Try with a smaller date range or different employee/location**
4. **Contact your system administrator**
5. **Check the system logs for detailed error information**

---

## 📈 Best Practices

### Report Planning

- **Regular Reviews**: Generate weekly/monthly reports for consistent tracking
- **Holiday Planning**: Use reports to plan holiday coverage
- **Performance Analysis**: Track employee working patterns over time
- **Compliance**: Maintain regular reports for audit purposes

### Data Management

- **Archive Old Reports**: Download and store important reports locally
- **Regular Cleanup**: Use data retention policies to manage database size
- **Backup Strategy**: Ensure important reports are backed up
- **Access Control**: Limit report access to authorized personnel

### Export Strategy

- **PDF for Sharing**: Use PDF format for presentations and formal documentation
- **Excel for Analysis**: Use Excel format for data analysis and calculations
- **Naming Convention**: Use consistent naming for downloaded files
- **Storage Organization**: Organize reports by date and type

---

_Last updated: {{ site.time | date: "%B %d, %Y" }}_
