---
layout: default
title: Reports System
description: Comprehensive reporting system including worked hours reports and custom report templates
---

# Reports System

The Reports System provides two powerful reporting capabilities: **Worked Hours Reports** for tracking employee time and **Report Templates** for collecting custom business data. Both systems support multiple export formats and role-based access control.

## Report Types

### 1. Worked Hours Reports

Generate comprehensive reports showing employee working hours, holiday data, and location-based summaries.

### 2. Report Templates

Create custom data collection forms that generate automated tasks and provide analytics dashboards with real-time insights.

---

# Report Templates System

## 🎯 What Are Report Templates?

Report Templates are **custom data collection forms** that allow you to gather structured business data from your employees on a regular basis. Think of them as digital forms that automatically create tasks for users to fill out, collect responses, and generate analytics dashboards.

### Key Features

- ✅ **Custom Fields**: Create forms with any fields you need (text, numbers, dates, booleans)
- ✅ **Automated Task Creation**: Background worker automatically creates tasks based on frequency
- ✅ **Real-time Analytics**: Live dashboard with submissions, charts, and insights
- ✅ **Multiple Export Formats**: PDF, Excel, and JSON exports
- ✅ **Role-based Access**: Control who can create templates and view analytics
- ✅ **Multi-tenant Support**: Each company manages their own templates

### Common Use Cases

| Template Type                    | Description                                           | Frequency |
| -------------------------------- | ----------------------------------------------------- | --------- |
| **Daily Sales Report**           | Track daily sales figures, customer counts, issues    | Daily     |
| **Weekly Inventory Check**       | Stock levels, item conditions, reorder needs          | Weekly    |
| **Monthly Safety Inspection**    | Safety compliance, incident reports, equipment status | Monthly   |
| **Customer Feedback Collection** | Service quality, satisfaction scores, comments        | As needed |
| **Equipment Maintenance Log**    | Equipment status, maintenance tasks, issues           | Weekly    |

---

## 🚀 How Report Templates Work

### 1. Template Creation Process

**Step 1: Create the Template**

- Admin/Manager creates a report template
- Defines custom fields (e.g., "Sales Amount", "Customer Count", "Notes")
- Sets collection frequency (daily, weekly, monthly)

**Step 2: User Assignment**

- Assign template to specific users or locations
- Set start date for data collection
- Define frequency (how often users need to fill it out)

**Step 3: Automated Task Generation**

- Background worker creates tasks automatically
- Tasks appear in user's task list when due
- Users receive notifications about pending reports

### 2. Data Collection Flow

```
Template Created → Users Assigned → Background Worker → Tasks Generated → Users Fill Forms → Data Stored → Analytics Updated
```

**Detailed Steps:**

1. **Background Worker Runs** (every 30 minutes)

   - Checks for assignments with due dates
   - Creates report tasks for assigned users
   - Sets proper due dates based on frequency

2. **User Sees Task**

   - Task appears in user's task dashboard
   - Shows as "Report Task" with template name
   - Includes description and due date

3. **User Fills Report**

   - Clicks "Fill Report" button
   - Form displays with custom fields from template
   - User enters data and submits

4. **Data Processing**
   - Submission stored in dynamic database table
   - Task marked as "COMPLETED"
   - Analytics dashboard updates in real-time

### 3. Analytics and Insights

**Real-time Dashboard Shows:**

- Total submissions count
- Submission trends over time
- Data by user and location
- Individual field analytics
- Export capabilities (PDF, Excel, JSON)

---

## 📋 Creating Report Templates

### Step 1: Access Template Management

1. **Navigate to Report Templates**

   - Go to main navigation → "Report Templates"
   - Requires `templates.create` permission

2. **Create New Template**
   - Click "Create Template" button
   - Enter template name and description

### Step 2: Define Template Fields

**Available Field Types:**

| Field Type  | Description     | Example Use                            |
| ----------- | --------------- | -------------------------------------- |
| **STRING**  | Text input      | Customer feedback, notes, descriptions |
| **NUMBER**  | Numeric input   | Sales amounts, quantities, scores      |
| **BOOLEAN** | Yes/No checkbox | Equipment working, task completed      |
| **DATE**    | Date picker     | Inspection date, delivery date         |

**Field Configuration:**

```json
{
  "name": "daily_sales",
  "inputType": "NUMBER",
  "required": true,
  "label": "Daily Sales Amount"
}
```

### Step 3: Save Template

- Review all fields and settings
- Click "Create Template"
- Template becomes available for assignment

---

## 👥 Assigning Templates to Users

### Assignment Process

1. **Select Template**

   - Go to template details page
   - Click "Assign to Users" button

2. **Configure Assignment**

   - **Select Users**: Choose which employees will fill this report
   - **Select Locations**: Assign to all users at specific locations
   - **Start Date**: When data collection should begin
   - **Frequency**: How often users need to submit (daily = 1, weekly = 7, monthly = 30)

3. **Background Task Generation**
   - System automatically creates tasks based on schedule
   - Users see tasks in their dashboard when due

### Assignment Example

**Daily Sales Report Assignment:**

- **Template**: "Daily Sales Report" (fields: Sales Amount, Customer Count, Notes)
- **Assigned to**: Store Managers at all retail locations
- **Start Date**: August 1st, 2025
- **Frequency**: Daily (every 1 day)

**Result**: Every day, each store manager gets a task to fill out the daily sales report.

---

## 📱 User Experience: Filling Out Reports

### 1. Task Notification

**Users see:**

- Task in dashboard: "Complete Report: Daily Sales Report"
- Due date and priority level
- "Fill Report" button

### 2. Report Form Interface

```
┌─────────────────────────────────────────────────────────┐
│              Complete Report: Daily Sales Report        │
├─────────────────────────────────────────────────────────┤
│                                                         │
│ Sales Amount (NUMBER): [_____________] €                │
│                                                         │
│ Customer Count (NUMBER): [_____________] customers      │
│                                                         │
│ Issues or Notes (STRING): [___________________]         │
│                          [___________________]         │
│                          [___________________]         │
│                                                         │
│ Equipment Working (BOOLEAN): ☑ Yes  ☐ No              │
│                                                         │
│               [Cancel]    [Submit Report]               │
└─────────────────────────────────────────────────────────┘
```

### 3. Submission Process

1. **Fill Required Fields**

   - All required fields must be completed
   - Validation happens in real-time

2. **Submit Report**
   - Click "Submit Report" button
   - Data is instantly saved
   - Task marked as completed
   - User returns to task dashboard

---

## 📊 Analytics Dashboard

### Accessing Analytics

1. **Navigate to Template**

   - Go to "Report Templates"
   - Click on template name
   - Select "Analytics" tab

2. **Permission Requirements**
   - Requires `templates.analytics.view` permission
   - Company-scoped access only

### Dashboard Components

**Summary Cards:**

- **Total Submissions**: Number of completed reports
- **Active Users**: Users who have submitted data
- **Date Range**: Current analytics period
- **Locations**: Number of locations with submissions

**Data Table:**
Each row shows:

- **Submission Date/Time**: When report was submitted
- **User Name**: Who submitted the report
- **Location**: Where the user is assigned
- **Field Data**: Individual columns for each template field

**Example Table:**
| Date | User | Location | Sales Amount | Customer Count | Notes |
|------|------|----------|--------------|----------------|-------|
| Aug 27, 11:13 PM | Ecaterina Pop | Bar 1 | €222 | 45 | Busy evening |
| Aug 27, 11:13 PM | Ion Popescu | Bar 1 | €5000 | 120 | Record sales! |

---

## 📥 Exporting Report Data

### Export Formats

**1. PDF Export**

- **Best for**: Presentations, printing, official documentation
- **Contains**: Formatted tables, summary data, professional layout
- **File naming**: `template-name-YYYY-MM-DD.pdf`

**2. Excel Export**

- **Best for**: Data analysis, calculations, integration with other tools
- **Contains**: Raw data in spreadsheet format, filterable columns
- **File naming**: `template-name-YYYY-MM-DD.xlsx`

**3. JSON Export**

- **Best for**: System integration, API consumption, data processing
- **Contains**: Structured data for programmatic access
- **File naming**: `template-name-YYYY-MM-DD.json`

### Export Process

1. **Access Analytics Dashboard**
2. **Select Date Range** (optional filters)
3. **Choose Export Format**
   - Click "Download PDF", "Download Excel", or "Download JSON"
4. **File Downloads Automatically**

### Export Data Structure

**PDF Format:**

```
Company Management Report
Template: Daily Sales Report
Period: August 1-31, 2025

Summary:
- Total Submissions: 87
- Active Users: 3
- Locations: 2

Detailed Data:
[Formatted table with all submissions]
```

**Excel Format:**

- **Sheet 1**: Summary data
- **Sheet 2**: Detailed submissions with individual columns
- **Sheet 3**: User and location breakdowns

---

## 🔐 Permissions and Access Control

### Required Permissions

**Template Management:**

- `templates.create` - Create new report templates
- `templates.read` - View template list
- `templates.update` - Modify existing templates
- `templates.delete` - Remove templates
- `templates.assign` - Assign templates to users

**Analytics Access:**

- `templates.analytics.view` - View analytics dashboards
- `templates.analytics.export` - Export report data

**Data Submission:**

- `tasks.complete` - Fill out and submit reports (via tasks)

### Access Levels

**Company Administrators:**

- Full access to all templates within their company
- Can create, modify, delete, and assign templates
- Access to all analytics and export capabilities

**Managers/Supervisors:**

- Can view templates they manage
- Access to analytics for their assigned templates
- Can assign templates to their team members

**Regular Users:**

- Can fill out reports assigned to them
- View their own submission history
- Cannot access analytics or template management

### Data Security

- **Company Isolation**: Each company only sees their own templates and data
- **Role-based Access**: Permissions control what users can do
- **Audit Trail**: All template actions are logged
- **Data Encryption**: Submissions stored securely in database

---

## ⚙️ Background Worker & Task Automation

### How Automated Task Creation Works

**Background Worker Process:**

1. **Runs Every 30 Minutes**

   - Checks all active report template assignments
   - Identifies assignments with due dates that have passed
   - Creates missing tasks for the date range

2. **Task Creation Logic**

   ```
   For each assignment:
   - Start from assignment.startDate
   - Create tasks for each frequency interval until today
   - Set individual due dates based on frequency
   - Store metadata linking tasks to templates
   ```

3. **Example Scenario**
   - **Assignment**: Daily sales report starting August 23rd
   - **Today**: August 27th
   - **Result**: Creates 5 tasks with due dates: 23rd, 24th, 25th, 26th, 27th

### Task Metadata System

Each generated task contains:

```json
{
  "type": "REPORT_TASK",
  "relatedEntityId": "assignment-id",
  "metadata": {
    "reportTemplateId": "template-uuid",
    "assignmentId": "assignment-uuid"
  }
}
```

This metadata enables:

- Proper analytics queries
- Template-specific task filtering
- Assignment tracking and management

### Frequency Options

| Frequency     | Days       | Use Case                    |
| ------------- | ---------- | --------------------------- |
| **Daily**     | 1          | Sales reports, daily checks |
| **Weekly**    | 7          | Inventory, team updates     |
| **Bi-weekly** | 14         | Performance reviews         |
| **Monthly**   | 30         | Compliance reports          |
| **Custom**    | Any number | Special reporting needs     |

---

## 🛠️ Technical Implementation

### Data Storage

**Report Template Structure:**

```sql
ReportTemplate {
  id: UUID
  name: STRING
  description: STRING
  companyId: UUID
  rows: ReportTemplateRow[]
}

ReportTemplateRow {
  id: UUID
  templateId: UUID
  name: STRING          -- Field name (e.g., "sales_amount")
  inputType: ENUM       -- STRING, NUMBER, BOOLEAN, DATE
}
```

**Dynamic Data Tables:**

- Each template creates a unique database table
- Table name: `report_data_${templateId}`
- Columns created dynamically based on template fields
- Includes metadata: userId, submittedAt, locationId

### API Integration

**Key Endpoints:**

- `POST /api/report-templates` - Create template
- `GET /api/report-templates/:id/analytics` - Get analytics data
- `POST /api/report-templates/:id/assign` - Assign to users
- `GET /api/report-templates/:id/export/:format` - Export data

### Background Processing

**Background Worker Service:**

- Prisma-based database queries
- Handles complex date calculations
- Creates tasks in batches for performance
- Updates assignment schedules automatically

---

## 📈 Best Practices

### Template Design

**Field Naming:**

- Use clear, descriptive names: "daily_sales_amount" not "amount"
- Avoid spaces and special characters in field names
- Keep names short but meaningful

**Field Types:**

- Use NUMBER for anything that needs calculations
- Use STRING for text that might be long (notes, descriptions)
- Use BOOLEAN for yes/no questions
- Use DATE for specific date inputs

### Assignment Strategy

**User Assignment:**

- Assign to specific users rather than large groups when possible
- Consider user workload and availability
- Set realistic frequencies based on business needs

**Date Planning:**

- Start assignments on logical business days (Monday for weekly reports)
- Consider holidays and vacation periods
- Plan for data collection gaps and backfilling

### Analytics Usage

**Regular Monitoring:**

- Check submission rates weekly
- Monitor for users who consistently miss deadlines
- Review data quality and completeness

**Data Analysis:**

- Export to Excel for complex calculations
- Use date filters to focus on specific periods
- Compare data across locations and users

---

## 🚨 Troubleshooting

### Common Issues

**Tasks Not Being Created:**

- Check that assignment start date is in the past
- Verify background worker is running (should run every 30 minutes)
- Ensure assignment is active and frequency is set correctly

**Users Can't See Tasks:**

- Verify user has `tasks.read` permission
- Check that user is properly assigned to the template
- Confirm user is in the correct company context

**Analytics Showing No Data:**

- Ensure users have actually submitted reports (completed tasks)
- Check date range filters in analytics
- Verify template has active assignments

**Export Failures:**

- Check that there is data to export
- Verify user has `templates.analytics.export` permission
- Try smaller date ranges for large datasets

### Getting Help

**For Technical Issues:**

1. Check system logs for background worker errors
2. Verify database connectivity and permissions
3. Review task creation and assignment tables
4. Contact system administrator

**For Business Process Issues:**

1. Review template design and field types
2. Check user training and understanding
3. Verify business process alignment
4. Consider frequency adjustments

---

# Worked Hours Reports

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
