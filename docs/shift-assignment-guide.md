---
layout: default
title: Shift Assignment Guide
description: Complete guide to creating and managing shift assignments
---

# Shift Assignment Guide

## Overview

This guide explains how to assign staff members to specific shifts using the Location Configuration system. This is the primary method for creating actual work schedules after setting up schedule templates.

## Key Concepts

### Templates vs. Assignments

1. **Schedule Templates**

   - Define shift patterns (time, duration, staff count)
   - Reusable across multiple dates
   - No actual staff assigned yet

2. **Shift Assignments**
   - Assign specific users to specific shifts
   - Create actual work schedules
   - Include validation and conflict checking

## Accessing Shift Assignment

### Prerequisites

Before you can assign shifts, you need:

1. **Location Created** - Basic location information set up
2. **Location Configured** - Off days and calendars configured
3. **Schedule Templates** - Shift patterns defined
4. **Staff Assigned** - Users assigned to the location

**Note**: Shift assignment is part of the **Location Configuration** process, not the initial location creation.

### Step 1: Navigate to Location Configuration

1. Login as a Location Manager or Administrator
2. Go to **Location Management**
3. Select your location
4. Click **Configuration** tab
5. Select **Shift Assignments** sub-tab

### Step 2: Choose Assignment Method

You have two options:

1. **Individual Assignment** - Assign one user to one shift
2. **Range Assignment** - Assign one user to multiple shifts across a date range

## Individual Shift Assignment

### When to Use

- Assigning coverage for specific dates
- One-time shift assignments
- Replacing staff for specific shifts
- Managing irregular schedules

### Step-by-Step Process

1. **Select Date and Shift**

   - Choose the date from the calendar
   - Select the shift template/time slot
   - Verify shift details (start time, end time, requirements)

2. **Choose Staff Member**

   - Select from available staff dropdown
   - System shows only eligible users
   - Users with conflicts are disabled/highlighted

3. **Validation Check**

   - System automatically checks:
     - User availability (no holidays/blocked time)
     - Shift conflicts (no overlapping assignments)
     - Role permissions (user can work this shift type)
     - Location access (user assigned to this location)

4. **Create Assignment**
   - Click **Assign** button
   - System creates the shift assignment
   - User receives notification (if enabled)
   - Assignment appears in calendar view

### Example: Single Shift Assignment

```
Date: March 15, 2025
Shift: Morning Shift (08:00 - 16:00)
User: Sarah Johnson
Status: ✅ Available - No conflicts
Result: Assignment created successfully
```

## Range Assignment

### When to Use

- Assigning regular weekly patterns
- Bulk assignment for consistent schedules
- Setting up recurring shifts
- Managing standard work patterns

### Step-by-Step Process

1. **Select Date Range**

   - Choose start date
   - Choose end date
   - Maximum range: 4 weeks

2. **Choose Shift Pattern**

   - Select shift template
   - Choose specific days of week (e.g., Monday-Friday)
   - Verify shift times and requirements

3. **Select Staff Member**

   - Choose user from dropdown
   - System shows availability summary for range
   - Conflicts highlighted in red

4. **Review and Confirm**

   - System shows preview of all assignments
   - Lists any conflicts or issues
   - Shows total shifts to be created

5. **Create Range Assignment**
   - Click **Create Range Assignment**
   - System creates all valid assignments
   - Skips dates with conflicts
   - Provides summary report

### Example: Range Assignment

```
Date Range: March 15 - March 28, 2025
Days: Monday, Wednesday, Friday
Shift: Afternoon Shift (14:00 - 22:00)
User: Mike Wilson
Conflicts: March 22 (user on holiday)
Result: 5 assignments created, 1 skipped
```

## System Validations

### Automatic Checks

The system performs these checks before creating assignments:

1. **User Availability**

   - No approved holidays during shift time
   - No blocked/unavailable periods
   - No existing shift assignments at same time

2. **Role Permissions**

   - User has required permissions for shift type
   - User assigned to this location
   - User role allows shift assignment

3. **Shift Constraints**

   - Shift template exists and is active
   - Location is operational on selected date
   - Not exceeding maximum staff for shift

4. **Business Rules**
   - Respects location off-days (weekly/specific dates)
   - Follows company scheduling policies
   - Maintains minimum/maximum shift lengths

### Validation Results

- ✅ **Valid**: Assignment created successfully
- ⚠️ **Warning**: Assignment created with notes (e.g., overtime)
- ❌ **Error**: Assignment blocked (conflict/rule violation)

## Managing Existing Assignments

### Viewing Assignments

1. **Calendar View**

   - See all assignments in calendar format
   - Color-coded by shift type or user
   - Click assignment to view details

2. **List View**
   - Detailed list of all assignments
   - Filter by date, user, or shift type
   - Sort by various criteria

### Editing Assignments

1. **Modify Assignment**

   - Click existing assignment
   - Change user, time, or date
   - System re-validates changes

2. **Delete Assignment**
   - Select assignment
   - Click delete/remove
   - Confirm deletion
   - User receives notification

### Assignment Status

- **Active**: Normal working assignment
- **Pending**: Awaiting confirmation
- **Cancelled**: Assignment removed
- **Completed**: Shift has been worked

## Holiday and Availability Integration

### How It Works

1. **Holiday Requests**

   - User submits holiday request
   - Manager approves request
   - System blocks user availability
   - Future assignments automatically prevented

2. **During Assignment**

   - System checks user availability in real-time
   - Users on approved holidays cannot be assigned
   - Existing assignments during holidays are automatically prevented

3. **When Holiday is Approved**

   - **Existing shifts are automatically deleted** from the user's schedule for the holiday period
   - **Holiday becomes visible in the calendar** as a blocked period
   - **User is marked unavailable** for the entire holiday duration
   - **No manual intervention required** - system handles cleanup automatically

4. **Calendar Integration**
   - **Approved holidays display** as visual blocks on the schedule calendar
   - **Shift assignments are prevented** during holiday periods
   - **User availability is updated** in real-time across all scheduling interfaces

### Best Practices

1. **Check Holidays First**

   - Review upcoming holidays before bulk assignment
   - Consider holiday patterns when planning
   - Use range assignment to automatically skip holiday dates

2. **Regular Review**
   - Weekly review of upcoming assignments
   - Check for new holiday approvals
   - Resolve conflicts promptly

## Common Scenarios

### Scenario 1: Regular Weekly Schedule

**Goal**: Assign Sarah to work Monday-Friday morning shifts for two weeks

**Steps**:

1. Use Range Assignment
2. Select date range (2 weeks)
3. Choose Monday-Friday
4. Select Morning Shift template
5. Assign to Sarah
6. System creates 10 assignments

### Scenario 2: Holiday Coverage

**Goal**: Mike is on holiday March 20-22, need coverage

**Steps**:

1. Use Individual Assignment
2. For each day (March 20, 21, 22)
3. Select Mike's usual shift
4. Assign to replacement staff
5. System validates no conflicts

### Scenario 3: New Staff Training

**Goal**: Train new employee with experienced staff

**Steps**:

1. Use Individual Assignment
2. Assign new employee to shifts
3. Ensure experienced staff on same shifts
4. Gradually increase responsibility

## Troubleshooting

### Common Issues

1. **User Not Available**

   - **Cause**: User on holiday or has conflicting assignment
   - **Solution**: Choose different user or date

2. **Permission Denied**

   - **Cause**: User lacks required role permissions
   - **Solution**: Update user role or choose different user

3. **Shift Template Missing**

   - **Cause**: No template defined for this time/location
   - **Solution**: Create schedule template first

4. **Location Access Error**
   - **Cause**: User not assigned to this location
   - **Solution**: Add user to location staff list

### Error Messages

- `User is not available during this period`: Check holiday calendar
- `Insufficient permissions`: Review user role assignments
- `Shift conflict detected`: Check for overlapping assignments
- `Location access denied`: Verify user location assignments

## Tips for Managers

### Efficient Assignment

1. **Use Templates**

   - Create templates for common shift patterns
   - Saves time on repeated assignments
   - Ensures consistency

2. **Plan Ahead**

   - Create assignments 2-4 weeks in advance
   - Allow time for holiday requests
   - Consider peak business periods

3. **Regular Patterns**
   - Use range assignment for regular schedules
   - Individual assignment for exceptions
   - Review and adjust monthly

### Communication

1. **Notify Staff**

   - System sends automatic notifications
   - Supplement with team meetings
   - Confirm receipt of important assignments

2. **Handle Conflicts**
   - Address scheduling conflicts promptly
   - Communicate changes clearly
   - Maintain backup coverage plans

## Support

For questions about shift assignment or technical issues:

1. Check this guide first
2. Contact your system administrator
3. Submit support ticket through the system
4. Refer to Location Management documentation

## Related Documentation

- [Schedule Templates](schedule-templates.md) - Creating reusable shift patterns
- [Locations](locations.md) - Location management and configuration
- [User Flows](user-flows.md) - General system workflows
- [Roles and Permissions](roles-and-permissions.md) - User access control
