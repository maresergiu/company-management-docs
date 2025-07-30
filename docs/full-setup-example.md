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

## 5. Adding Users

Navigate to: User Management > Create User

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

## 6. User Configuration

Navigate to: Users > Sarah Johnson > Configuration

Set manager details:

```
Contact Number: +1 234-567-8901
Emergency Contact: +1 234-567-8902
Availability: Full-time
```

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

## 8. Setting Up Location

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

## 9. Location Configuration

Navigate to: Locations > Coffee Express Downtown > Configuration

### Operating Hours

```
Monday-Friday: 07:00 - 22:00
Saturday: 08:00 - 23:00
Sunday: 09:00 - 20:00
```

### Staff Requirements

```
Weekday Morning: 3 staff
Weekday Evening: 2 staff
Weekend Morning: 4 staff
Weekend Evening: 3 staff
```

## Next Steps

After this initial setup:

1. Location manager can log in
2. Create schedules using template
3. Staff can view their schedules
4. Holiday requests can be managed
