---
layout: default
title: Schedule Templates
description: Creating and using reusable schedule templates
---

# Schedule Templates

## Overview

Schedule templates help create consistent shift patterns. They define a set of shifts that can be reused when creating schedules, saving time and ensuring consistency.

## Template Components

A schedule template consists of:

1. **Basic Information**

   - Template name
   - Description

2. **Shifts**
   - Shift name
   - Start time
   - End time
   - Number of staff needed

## Creating a Template

1. **Required Information**

   - Template name (2-50 characters)
   - Description
   - At least one shift

2. **For Each Shift**

   - Name (2-50 characters)
   - Start time
   - End time
   - Staff count (1-100 people)

3. **Validation Rules**
   - Template must have at least one shift
   - All shifts must have valid times
   - Staff count must be between 1 and 100
   - Overnight shifts are allowed (end time can be before start time)

## Using Templates

When creating a schedule:

1. Select a template
2. The system creates shifts based on the template pattern
3. Assign staff to the generated shifts

## Benefits

- Consistent shift patterns across schedules
- Quick schedule creation
- Standardized staff requirements
- Reduced scheduling errors

# Schedule Template Example

This guide provides a practical example of creating and using a schedule template.

## Example: Creating a "Standard Week" Template

Let's create a template for a standard work week with morning and afternoon shifts.

### Step 1: Access Templates

1. Log in as an administrator
2. Go to Schedule Templates section
3. Click "Create Template"

### Step 2: Basic Information

Fill in the template details:

```
Name: Standard Week Template
Description: Standard morning and afternoon shifts for weekdays
```

### Step 3: Define Shifts

Add two shifts:

1. **Morning Shift**

   ```
   Name: Morning Shift
   Start Time: 08:00
   End Time: 16:00
   Staff Needed: 3
   ```

2. **Afternoon Shift**
   ```
   Name: Afternoon Shift
   Start Time: 16:00
   End Time: 00:00
   Staff Needed: 2
   ```

### Step 4: Using the Template

1. Go to Schedule Management
2. Click "Create Schedule"
3. Select "Standard Week Template"
4. The system will create:
   - Morning shift (8 AM - 4 PM) needing 3 staff
   - Afternoon shift (4 PM - 12 AM) needing 2 staff

### Step 5: Assign Staff

After creating the schedule template, you need to create actual shift assignments:

1. Go to Location Configuration → Shift Assignments
2. Use Individual Assignment for specific dates
3. Use Range Assignment for recurring patterns
4. System validates availability and prevents conflicts

**For detailed assignment process, see [Shift Assignment Guide](shift-assignment-guide.md)**

## Tips for Admins

1. **Naming Convention**

   - Use clear, descriptive names
   - Include shift pattern in the name
   - Example: "Standard Week - 2 Shifts"

2. **Staff Count**

   - Consider peak hours
   - Account for breaks
   - Plan for minimum coverage

3. **Time Settings**
   - Use 24-hour format
   - Consider overlap for handovers
   - Plan for shift transitions

## Common Use Cases

1. **Regular Week**

   - Morning and afternoon shifts
   - Fixed staff requirements
   - Standard working hours

2. **Weekend Coverage**

   - Different shift patterns
   - Adjusted staff numbers
   - Special hours

3. **Holiday Schedule**
   - Modified shift times
   - Adjusted staff count
   - Special requirements

## Support

For questions about creating or using schedule templates, contact your system administrator.

## Support

For questions about schedule templates or to request changes, contact your system administrator.
