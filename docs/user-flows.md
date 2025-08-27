---
layout: default
title: User Flows
description: Typical workflows for different user types
---

# User Flows

This document explains how different types of users interact with the system.

## Super Administrator Flow

### Initial Access

1. Login with super admin credentials
2. Lands on system dashboard
3. Has access to all companies

### Key Actions

- Switch between different companies
- Create new companies
- Manage company administrators
- Access all features across all companies
- View system-wide settings

### Company Management

1. Can select any company from dropdown
2. Views selected company's dashboard
3. Has full access to company features
4. Can switch to another company anytime

## Company Administrator Flow

### Initial Access

1. Login with admin credentials
2. Lands on company dashboard
3. Access limited to their own company

### Key Actions

- Manage company users
- Create and manage locations (Step 1: Location Creation)
- Create custom roles
- Assign permissions
- View company settings

**Note**: Company administrators typically handle the initial location creation, while location managers handle the configuration and shift assignments.

### User Management

1. **Create new users** (Step 1: Basic system setup)
2. **Configure user profiles** (Step 2: Detailed employment setup)
3. Assign roles to users
4. Manage user permissions
5. Handle user access

**Note**: Company administrators typically handle user creation, while HR or users themselves handle detailed profile configuration.

## Location Manager Flow

### Initial Access

1. Login with location manager credentials
2. Lands on location dashboard
3. Access limited to assigned locations

### Key Actions

- Configure location settings (Step 2: Location Configuration)
- Set up off days and holidays
- Create shift calendars
- Assign staff to shifts
- Monitor location schedules

**Note**: Location managers handle the operational configuration of locations after they've been created by administrators.

## Regular User Flow

### Initial Access

1. Login with user credentials
2. Lands on personal dashboard
3. Access based on assigned permissions

### Schedule Management

1. View personal schedule
2. See assigned locations
3. Submit holiday requests
4. Receive notifications for new shift assignments

**Note**: Location managers can create shift assignments via Location Configuration. See [Shift Assignment Guide](shift-assignment-guide.md) for details.

### Holiday Requests

1. Create new holiday request
2. View request status:
   - Pending (waiting for approval)
   - Approved (request accepted)
   - Rejected (request denied)
3. View holiday history

### Location Access

1. View assigned locations
2. See location schedules
3. Access based on permissions

### Reports (if permitted)

**Worked Hours Reports:**

1. Access Reports section from main navigation
2. Select Worked Hours Report
3. Configure report parameters:
   - Choose grouping (by employee or location)
   - Select target employee or location
   - Set date range
4. Generate preview
5. Export as PDF or Excel

**Report Template Tasks:**

1. View assigned report tasks in Tasks dashboard
2. Click "Fill Report" for pending report tasks
3. Complete custom form with required fields
4. Submit report data
5. Task automatically marked as completed

---

# Report Template User Scenarios

## Scenario 1: Restaurant Manager - Daily Sales Reporting

### Background

**Maria** is a restaurant manager at "Downtown Bistro" who needs to submit daily sales reports to corporate headquarters.

### User Journey

**Day 1 - Assignment Setup (Done by Admin):**

1. **Company Admin** creates "Daily Sales Report" template
   - Fields: Sales Amount (NUMBER), Customer Count (NUMBER), Special Events (STRING), Issues (STRING)
2. **Admin assigns** template to Maria starting August 23rd, frequency: Daily
3. **Background worker** creates tasks for Maria automatically

**Day 1-5 - Maria's Daily Routine:**

1. **Maria logs in** at end of each day
2. **Sees task**: "Complete Report: Daily Sales Report" (Due: Today)
3. **Clicks "Fill Report"** button
4. **Completes form**:
   - Sales Amount: €1,250
   - Customer Count: 45
   - Special Events: "Live music night"
   - Issues: "Coffee machine needs repair"
5. **Submits report** - Task automatically completed
6. **Repeats daily** - New task appears each day

**Weekly Review (Manager/Corporate):**

1. **Regional Manager** accesses analytics dashboard
2. **Views submissions** from all restaurant managers
3. **Exports Excel** report for corporate analysis
4. **Identifies trends** and performance patterns

### Business Value

- **Consistent Data Collection**: Every day, same format
- **Real-time Insights**: Corporate sees data immediately
- **Automated Workflow**: No manual reminders needed
- **Historical Analysis**: Track performance over time

---

## Scenario 2: Retail Store - Weekly Inventory Check

### Background

**James** works at multiple retail locations and needs to perform weekly inventory checks for stock management.

### User Journey

**Setup Phase:**

1. **Store Manager** creates "Weekly Inventory Check" template
   - Fields: Low Stock Items (STRING), Damaged Goods (NUMBER), Reorder Needed (BOOLEAN), Notes (STRING)
2. **Assigns to all store staff** at 3 locations, starts Monday, frequency: Weekly (7 days)

**Weekly Execution:**

1. **Monday morning**: James sees inventory task in dashboard
2. **Goes through store** checking stock levels
3. **Fills report**:
   - Low Stock Items: "T-shirts size M, Jeans 32x30"
   - Damaged Goods: 3
   - Reorder Needed: ✓ Yes
   - Notes: "Shipment delayed due to holiday weekend"
4. **Submits report** before end of shift

**Management Analytics:**

1. **Store Manager** reviews all submissions weekly
2. **Identifies patterns** across locations
3. **Plans purchasing** based on reorder flags
4. **Tracks damage rates** for loss prevention

### Business Value

- **Inventory Control**: Prevent stockouts
- **Multi-location Oversight**: Consistent process across stores
- **Purchasing Optimization**: Data-driven reorder decisions
- **Loss Prevention**: Track and analyze damage patterns

---

## Scenario 3: Construction Site - Safety Inspection Reports

### Background

**Alex** is a site supervisor responsible for daily safety inspections at construction projects.

### User Journey

**Template Creation:**

1. **Safety Manager** creates "Daily Safety Inspection" template
   - Fields: Hard Hats Count (NUMBER), Safety Violations (NUMBER), Equipment Status (BOOLEAN), Incident Report (STRING)
2. **Assigns to all site supervisors**, starts project date, frequency: Daily

**Daily Safety Routine:**

1. **Morning inspection**: Alex walks the construction site
2. **Checks safety compliance** across all areas
3. **Opens task**: "Complete Report: Daily Safety Inspection"
4. **Documents findings**:
   - Hard Hats Count: 23
   - Safety Violations: 1
   - Equipment Status: ✓ All working
   - Incident Report: "Worker forgot hard hat in parking area - reminded about policy"
5. **Submits immediately** for compliance records

**Compliance Tracking:**

1. **Safety Manager** monitors all sites daily
2. **Tracks violation trends** across projects
3. **Generates compliance reports** for authorities
4. **Identifies training needs** based on violation patterns

### Business Value

- **Regulatory Compliance**: Meet safety reporting requirements
- **Risk Management**: Early identification of safety issues
- **Documentation**: Complete audit trail for inspections
- **Continuous Improvement**: Data-driven safety training

---

## Scenario 4: Customer Service - Monthly Feedback Collection

### Background

**Sofia** manages customer service for an e-commerce company and needs to collect monthly team performance data.

### User Journey

**Monthly Process:**

1. **Customer Service Manager** creates "Monthly Team Performance" template
   - Fields: Tickets Resolved (NUMBER), Customer Satisfaction (NUMBER), Training Hours (NUMBER), Improvement Ideas (STRING)
2. **Assigns to team leads**, starts first of month, frequency: Monthly (30 days)

**End-of-Month Reporting:**

1. **Sofia receives task** on last day of month
2. **Compiles team data** from various systems
3. **Completes comprehensive report**:
   - Tickets Resolved: 847
   - Customer Satisfaction: 4.8/5.0
   - Training Hours: 12
   - Improvement Ideas: "Implement chatbot for common questions"
4. **Submits before deadline**

**Strategic Planning:**

1. **Department Head** reviews all team reports
2. **Compares performance** across teams
3. **Plans training programs** based on needs
4. **Implements improvement suggestions**

### Business Value

- **Performance Tracking**: Consistent metrics across teams
- **Strategic Planning**: Data-driven decision making
- **Continuous Improvement**: Capture and act on team suggestions
- **Resource Allocation**: Identify training and support needs

---

## Scenario 5: Healthcare Facility - Equipment Maintenance Logs

### Background

**Dr. Chen** oversees medical equipment at a clinic and must maintain regular equipment inspection logs for regulatory compliance.

### User Journey

**Compliance Setup:**

1. **Facility Manager** creates "Equipment Maintenance Log" template
   - Fields: Equipment ID (STRING), Status Check (BOOLEAN), Maintenance Needed (BOOLEAN), Issues Found (STRING), Next Service Date (DATE)
2. **Assigns to medical staff**, starts immediately, frequency: Weekly

**Weekly Equipment Checks:**

1. **Dr. Chen performs** systematic equipment inspection
2. **Opens maintenance task** in system
3. **Records detailed findings**:
   - Equipment ID: "X-RAY-001"
   - Status Check: ✓ Operational
   - Maintenance Needed: ☐ No
   - Issues Found: "None detected"
   - Next Service Date: 2025-09-15
4. **Submits for compliance** record

**Regulatory Reporting:**

1. **Compliance Officer** exports monthly reports
2. **Maintains audit trail** for regulatory inspections
3. **Schedules maintenance** based on reported needs
4. **Tracks equipment lifecycle** and replacement planning

### Business Value

- **Regulatory Compliance**: Meet healthcare equipment standards
- **Patient Safety**: Ensure all equipment is functioning properly
- **Maintenance Planning**: Proactive equipment servicing
- **Audit Readiness**: Complete documentation for inspections

---

## Scenario 6: Permission-Based UI Customization - Multi-Role Company

### Background

**TechCorp Solutions** is a growing company with different employee types who need different levels of access. The permission system dynamically shapes what each user sees in their interface.

### User Journey

### **Character 1: Sarah (Company Administrator)**

**Permissions**: All permissions (Administrator role)

**Sarah's Login Experience:**

1. **Logs in** → Sees **full navigation menu**:

   ```
   Dashboard
   ├── Users           (users.read, users.create, users.update, users.delete)
   ├── Locations       (locations.read, locations.create, locations.update)
   ├── Schedule Templates (schedules.read, schedules.create)
   ├── Tasks           (tasks.read, tasks.approve, tasks.assign)
   ├── Reports         (reports.read)
   ├── Report Templates (templates.create, templates.assign, templates.analytics.view)
   ├── Roles           (roles.create, roles.read, roles.update)
   └── Settings        (settings.read)
   ```

2. **Creates Custom Role** for Store Managers:

   - ✅ `locations.read` - View store information
   - ✅ `templates.read` - See assigned report templates
   - ✅ `templates.analytics.view` - View analytics for their templates
   - ✅ `tasks.read` - See their report tasks
   - ❌ `users.create` - Cannot create new employees
   - ❌ `templates.create` - Cannot create new templates

3. **Assigns users** to the "Store Manager" role

---

### **Character 2: Mike (Store Manager)**

**Permissions**: Limited set assigned by Sarah

**Mike's Login Experience:**

1. **Logs in** → Sees **restricted navigation menu**:

   ```
   Dashboard
   ├── Locations       (can view only - no create/edit buttons)
   ├── Tasks           (sees only report tasks assigned to him)
   ├── Report Templates (sees analytics for templates he manages)
   └── [Users, Roles, Settings sections completely hidden]
   ```

2. **Report Templates Page**:

   - **Can View**: Analytics dashboards for "Daily Sales Report"
   - **Can Export**: PDF and Excel reports (has templates.analytics.view)
   - **Cannot See**: "Create Template" button (missing templates.create)
   - **Cannot See**: "Assign to Users" button (missing templates.assign)

3. **Tasks Dashboard**:
   - **Sees**: His daily sales report tasks
   - **Can Complete**: Fill out report forms
   - **Cannot See**: Other users' tasks or holiday approval requests

---

### **Character 3: Emma (Store Employee)**

**Permissions**: Minimal set for daily operations

**Emma's Login Experience:**

1. **Logs in** → Sees **minimal navigation menu**:

   ```
   Dashboard
   ├── My Schedule     (schedules.view.own only)
   ├── Tasks           (tasks.read - sees only her assigned tasks)
   └── [All management sections hidden]
   ```

2. **Tasks Dashboard**:

   - **Sees**: Only her report tasks: "Complete Report: Daily Sales Report"
   - **Can Complete**: Fill out forms when tasks are assigned
   - **Cannot See**: Analytics, other users' tasks, template management

3. **No Access To**:
   - Report Templates section (missing all templates.\* permissions)
   - User management (missing users.\* permissions)
   - Analytics dashboards (missing templates.analytics.view)

---

### **Character 4: David (Regional Manager)**

**Permissions**: Analytics-focused permissions

**David's Login Experience:**

1. **Logs in** → Sees **analytics-focused menu**:

   ```
   Dashboard
   ├── Reports         (reports.read)
   ├── Report Templates (templates.analytics.view, templates.analytics.export)
   ├── Locations       (locations.read)
   └── [User/Role management hidden]
   ```

2. **Report Templates Analytics**:

   - **Can View**: All analytics for templates across multiple locations
   - **Can Export**: Advanced exports in PDF, Excel, JSON formats
   - **Cannot Create**: New templates (missing templates.create)
   - **Cannot Assign**: Templates to users (missing templates.assign)

3. **Advanced Analytics**:
   - **Sees**: Cross-location performance comparisons
   - **Can Filter**: By date ranges, users, locations
   - **Exports**: Executive-level reports for corporate

---

## Permission-Driven UI Examples

### **Navigation Menu Transformation**

**Full Admin View (Sarah):**

```
☰ Menu
├── 👥 Users              [Create User] [Import Users]
├── 📍 Locations          [Add Location] [Bulk Edit]
├── 📅 Schedule Templates [Create Template] [Assign Shifts]
├── ✅ Tasks              [Approve All] [Assign Tasks]
├── 📊 Reports            [Generate] [Export]
├── 📋 Report Templates   [Create] [Assign] [Analytics]
├── 🛡️ Roles             [Create Role] [Edit Permissions]
└── ⚙️ Settings          [Company Settings] [Integrations]
```

**Store Manager View (Mike):**

```
☰ Menu
├── 📍 Locations          [View Only]
├── ✅ Tasks              [My Tasks Only]
└── 📋 Report Templates   [Analytics Only]
```

**Employee View (Emma):**

```
☰ Menu
├── 📅 My Schedule        [View Only]
└── ✅ Tasks              [My Tasks Only]
```

### **Button-Level Permission Control**

**Report Templates Page for Different Users:**

**Sarah (Admin):**

```
[+ Create Template] [📊 Analytics] [👥 Assign Users] [🗑️ Delete] [📝 Edit]
```

**Mike (Store Manager):**

```
[📊 Analytics] [📥 Export]
```

**Emma (Employee):**

```
[No buttons shown - page not accessible]
```

### **Data Filtering by Permissions**

**Analytics Dashboard - What Each User Sees:**

**Sarah (Admin):**

- All templates across all locations
- All user submissions
- Company-wide analytics
- Full export capabilities

**Mike (Store Manager):**

- Only templates he's assigned to manage
- Only submissions from his store/team
- Location-specific analytics
- Export for his data only

**David (Regional Manager):**

- All templates in his region
- Cross-location comparisons
- Regional performance metrics
- Executive-level exports

**Emma (Employee):**

- No access to analytics dashboard
- Only sees her own task completion history

---

## Business Impact of Permission System

### **Security Benefits**

- **Data Protection**: Users only see data they need
- **Role Separation**: Clear boundaries between responsibilities
- **Audit Compliance**: Track who can access what information

### **User Experience Benefits**

- **Clean Interface**: No confusing buttons/menus for unavailable features
- **Focused Workflow**: Users see only relevant tools for their job
- **Reduced Training**: Simpler interfaces require less onboarding

### **Operational Benefits**

- **Delegation**: Admins can safely delegate specific responsibilities
- **Scalability**: Easy to add new roles as company grows
- **Flexibility**: Permissions can be adjusted without code changes

### **Real-World Permission Combinations**

**"Store Manager" Role:**

- ✅ View store information and locations
- ✅ View analytics dashboards for their reports
- ✅ Export data (PDF, Excel) for their store
- ✅ See and complete their assigned tasks
- ✅ View their own schedules
- ❌ Create new report templates
- ❌ Manage users or create accounts

**Result**: Can view analytics and export data for their store, but cannot create templates or manage users.

**"Data Analyst" Role:**

- ✅ View all analytics dashboards across the company
- ✅ Export all report data in multiple formats
- ✅ Generate worked hours reports
- ✅ View all location information
- ❌ Create or modify report templates
- ❌ Assign tasks or manage operations
- ❌ Manage users or roles

**Result**: Full analytics access across all data, but cannot create templates or manage operations.

**"Team Lead" Role:**

- ✅ View all tasks in the system
- ✅ Assign report tasks to team members
- ✅ View existing report templates
- ✅ See team schedules and assignments
- ❌ View analytics dashboards
- ❌ Create new templates
- ❌ Export report data

**Result**: Can assign report tasks to team members and view schedules, but cannot access analytics or create templates.

---

## Permission Testing Scenarios

### **Scenario: Adding New Store Manager**

1. **Sarah creates** "Mike" as new user
2. **Assigns "Store Manager" role** with limited permissions
3. **Mike logs in** → Sees only store-specific features
4. **Tries to access** User Management → Gets "Access Denied"
5. **Can complete** daily sales reports successfully
6. **Can view** analytics for his store only

### **Scenario: Promoting Employee to Manager**

1. **Emma (Employee)** currently sees minimal interface
2. **Sarah updates** Emma's role to "Store Manager"
3. **Emma logs out and back in**
4. **New navigation** automatically appears with analytics access
5. **Previous restrictions** removed, new permissions active
6. **UI transforms** without any technical changes needed

### **Scenario: Temporary Analytics Access**

1. **David needs** specific data for quarterly review
2. **Sarah temporarily adds** `templates.analytics.export` permission
3. **David gains** export capabilities immediately
4. **Completes analysis** and exports needed reports
5. **Sarah removes** permission after project completion
6. **David's interface** reverts to previous state

This demonstrates how the **permission system is the backbone** of your entire platform - it doesn't just control security, it **shapes every user's entire experience**!

---

## Cross-Scenario Common Patterns

### For All Users (Data Submitters)

1. **Login** → **Check Tasks** → **Fill Reports** → **Submit Data**
2. **Consistent Interface**: Same process regardless of report type
3. **Mobile Friendly**: Can complete on any device
4. **Automatic Completion**: No manual approval needed

### For Managers/Analysts

1. **Access Analytics** → **Review Data** → **Export Reports** → **Make Decisions**
2. **Real-time Dashboards**: See submissions as they happen
3. **Multiple Export Formats**: PDF for presentations, Excel for analysis
4. **Permission-based Access**: Only see relevant data

### System Automation

1. **Background Worker**: Creates tasks automatically
2. **No Manual Reminders**: System handles scheduling
3. **Consistent Data Collection**: Same format every time
4. **Scalable Process**: Works for any number of users/locations

## Common Features for All Users

### Profile Management

- View personal profile
- Update contact information
- Change password
- Enable/disable 2FA

### Navigation

- Use main menu for accessible features
- View only permitted sections
- Access help/support

### Session Management

- Automatic logout after inactivity
- Manual logout option
- Session security features
