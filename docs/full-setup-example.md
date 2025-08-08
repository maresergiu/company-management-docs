---
layout: default
title: Complete Setup Guide
description: Step-by-step walkthrough from registration to full configuration
---

# Full Setup Example: Coffee Shop Chain

This example walks through setting up a coffee shop chain "Coffee Express" with multiple locations.

## 1. Company Registration

Visit: `https://your-domain.com/register`

Enter company details:

```
Company Name: Coffee Express Ltd.
Company Email: admin@coffeeexpress.com
Admin Name: John Smith
Admin Email: john.smith@coffeeexpress.com
Password: ********
```

## 2. Email Verification

1. Check email: `john.smith@coffeeexpress.com`
2. Click verification link
3. System confirms: "Email verified successfully"

## 3. First Login

Visit: `https://your-domain.com/login`

```
Email: john.smith@coffeeexpress.com
Password: ********
```

## 4. Creating Roles

Navigate to: Role Management > Create Role

Create Location Manager role:

```
Role Name: Location Manager
Description: Manages single location operations

Permissions:
- locations.configuration.view
- locations.configuration.manage
- schedules.create
- schedules.read
- schedules.update
- users.holiday.approve
```

Create Staff role:

```
Role Name: Staff Member
Description: Regular staff permissions

Permissions:
- schedules.view.own
- users.holiday.request
```

## 5. Creating Users

Navigate to: User Management > Create User

**This step establishes users as system members with basic access and permissions.**

Add Location Manager:

```
Name: Sarah Johnson
Email: sarah.j@coffeeexpress.com
Role: Location Manager
```

Add Staff Member:

```
Name: Mike Wilson
Email: mike.w@coffeeexpress.com
Role: Staff Member
```

**This creates the basic user accounts with essential access and role information.**

## 6. Configuring Users

Navigate to: Users > Sarah Johnson > Configuration

**This step sets up the detailed employment profiles for the users.**

Set manager details:

```
Phone: +1 234-567-8901
Address: "123 Main Street, Downtown"
Date of Birth: "1990-05-15"
Nationality: "Canadian"
Emergency Contact: { name: "John Johnson", phone: "+1 234-567-8902", relationship: "Spouse" }

```

**This configuration defines the complete employment profile and personal details.**

## 7. Creating Schedule Template

Navigate to: Schedule Templates > Create Template

Create weekday template:

```
Name: Weekday Standard
Description: Standard weekday shifts

Shifts:
1. Morning Shift
   - Start: 07:00
   - End: 15:00
   - Staff: 3

2. Evening Shift
   - Start: 15:00
   - End: 22:00
   - Staff: 2
```

## 8. Creating the Location

Navigate to: Location Management > Create Location

Enter location details:

```
Name: Coffee Express Downtown
Address: 123 Main Street, Downtown
Contact: +1 234-567-8900
Status: Active
```

Assign users to location:

```
Location Manager: Sarah Johnson
Staff Members: Mike Wilson
```

Assign schedule templates:

```
Default Template: Weekday Standard
```

**This creates the basic location with essential business information.**

## 9. Configuring the Location

Navigate to: Locations > Coffee Express Downtown > Configuration

**This step sets up the operational scheduling rules for the location.**

### Off Days Configuration

```
Weekly Off Days: Sunday (location closed)
Specific Off Dates: Dec 25, Jan 1 (holidays)
```

### Calendar Setup

Create shift calendars based on the Weekday Standard template:

```
Morning Shift Calendar: 07:00 - 15:00
Evening Shift Calendar: 15:00 - 22:00
```

### Staff Requirements

```
Weekday Morning: 3 staff
Weekday Evening: 2 staff
Weekend Morning: 4 staff
Weekend Evening: 3 staff
```

**This configuration defines how the location operates for scheduling purposes.**

## Next Steps

After this initial setup:

1. Location manager can log in
2. Create actual shift assignments using templates
3. Use Location Configuration → Shift Assignments for:
   - Individual shift assignments
   - Range assignments for recurring patterns
4. Staff can view their assigned schedules
5. Holiday requests can be managed with automatic availability checking

### Creating Your First Shift Assignment

1. Go to Location Management → Coffee Express Downtown → Configuration
2. Click Shift Assignments tab
3. Use Individual Assignment to assign Mike Wilson to tomorrow's Morning Shift
4. System validates availability and creates assignment
5. Mike receives notification of new assignment

**For complete assignment process, see [Shift Assignment Guide](shift-assignment-guide.md)**
