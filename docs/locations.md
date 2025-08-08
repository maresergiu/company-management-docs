---
layout: default
title: Locations
description: Managing multiple business locations
---

# Locations in the System

## Overview

Locations are physical places where staff work. Each company can have multiple locations, and each location can have its own schedules, staff, and settings.

## Location States

A location can be in one of three states:

1. **Active**

   - Fully operational location
   - Has established schedules
   - Has assigned staff
   - Regular operations ongoing

2. **Sleep**

   - Temporarily deactivated location
   - Maintains its configuration
   - No active schedules
   - Can be reactivated when needed

3. **Process**
   - Location in setup phase
   - Initial configuration ongoing
   - Not yet ready for operations
   - Pending final activation

## Location Management

### Understanding the Two-Step Process

Location management in our system follows a **two-step process**:

1. **Creating a Location** - Basic business setup
2. **Configuring a Location** - Operational scheduling setup

This separation allows for proper role separation and operational flexibility.

### Step 1: Creating a Location

**Purpose**: Establish the location as a physical workplace with basic operational details.

**What it includes**:

- **Basic Information**: Name, address, city, country, postal code, phone, email
- **Status**: Active, inactive, maintenance
- **Manager Assignment**: Assign a location manager
- **Staff Assignment**: Assign users to work at this location
- **Schedule Templates**: Link existing templates to the location

**When to do this**: When setting up a new business location or adding a new workplace to your company.

### Step 2: Configuring a Location

**Purpose**: Define how the location operates for scheduling purposes.

**What it includes**:

- **Off Days Weekly**: Which days of the week the location is closed (e.g., Sunday = 0, Saturday = 6)
- **Off Dates Specific**: Specific dates when location is closed (holidays, maintenance days)
- **Calendar Management**: Create and manage shift calendars
- **Shift Assignments**: Assign staff to specific shifts
- **Operational Rules**: Business rules for scheduling

**When to do this**: After creating the location, when ready to set up operational scheduling.

### Why This Two-Step Design?

#### **✅ Separation of Concerns**

- **Creation**: Basic business setup (where, who, contact info)
- **Configuration**: Operational scheduling rules (when, how, patterns)

#### **✅ Flexibility**

- Can create a location without configuring it immediately
- Can reconfigure operational settings without changing basic info
- Different users might handle creation vs. configuration

#### **✅ Data Integrity**

- Basic location info rarely changes
- Operational settings change more frequently
- Separate validation rules for each

#### **✅ Role Separation**

- **Location Creation**: Usually handled by admins/managers
- **Location Configuration**: Usually handled by location managers

### Practical Example: Coffee Shop Setup

Let's walk through setting up a new coffee shop location:

#### **Step 1: Create Location** (Admin does this)

```
Location: "Coffee Express Downtown"
Address: "123 Main Street, Downtown"
Contact: +1 234-567-8900
Manager: Sarah Johnson
Staff: Mike Wilson, John Doe
Status: Active
Schedule Templates: Weekday Standard, Weekend Standard
```

#### **Step 2: Configure Location** (Location Manager does this)

```
Off Days: Sunday (closed)
Specific Off Dates: Dec 25, Jan 1 (holidays)
Calendars: Morning Shift Calendar, Evening Shift Calendar
Shift Assignments: Mike works Mon-Fri mornings, John works Mon-Fri evenings
```

#### **Result**

- **Creation**: Establishes the physical location with basic info
- **Configuration**: Sets up operational scheduling for the location

### Location Settings

Each location can have its own:

- Operating hours
- Staff requirements
- Schedule templates
- Manager assignments
- Contact information

## Staff and Locations

### Staff Assignment Rules

1. **Basic Rules**:

   - Staff can be assigned to multiple locations
   - Each shift must be at one location
   - Staff can't have overlapping shifts at different locations

2. **Assignment Types**:
   - Primary location (main workplace)
   - Secondary locations (additional workplaces)
   - Temporary assignments

### Users with Location Management Permissions

Users with location management permissions can:

- View location schedules
- Create shift assignments via Location Configuration
- Use Individual Assignment for specific shifts
- Use Range Assignment for recurring patterns
- Monitor attendance and resolve conflicts

**Note**: These capabilities are determined by the user's assigned permissions, not by a specific "Location Manager" role. See [Roles and Permissions](roles-and-permissions.md) for details on permission-based access control.

**For complete shift assignment process, see [Shift Assignment Guide](shift-assignment-guide.md)**

## Schedules and Locations

### Schedule Management

1. **Location Schedules**:

   - Each location has its own schedules
   - Can use schedule templates
   - Customizable to location needs
   - Visible to assigned staff

2. **Schedule Features**:
   - Weekly/monthly views
   - Staff rotation options
   - Holiday management
   - Shift templates

## Location Access

### Permission Levels

1. **View Access**:

   - See location details
   - View schedules
   - See staff assignments

2. **Management Access**:

   - Edit location settings
   - Manage schedules
   - Assign staff
   - Create/edit shifts

3. **Admin Access**:
   - Full location control
   - Configure settings
   - Manage permissions
   - Access all features

## Support

For questions about locations or to request changes, contact your system administrator.
