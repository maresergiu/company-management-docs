---
layout: default
title: User Types
description: Common user roles and their responsibilities
---

# User Types and Their Roles

## Overview

In our platform, users are defined by their permissions rather than fixed roles. However, there are some common user types based on typical permission combinations.

## User Creation vs Configuration

### Understanding the Two-Step Process

User management in our system follows a **two-step process**:

1. **Creating a User** - Basic system setup
2. **Configuring a User** - Detailed profile setup

This separation allows for proper role separation and operational flexibility.

### Step 1: Creating a User

**Purpose**: Establish the user as a system member with basic access and permissions.

**What it includes**:

- **Basic Information**: Email, password, firstName, lastName
- **Role Assignment**: Assign roles to the user
- **Company Association**: Link user to company
- **Default Holiday Allowance**: Create initial holiday allowance (0 days)

**When to do this**: When setting up a new employee in the system or adding a new user to your company.

### Step 2: Configuring a User

**Purpose**: Define the user's complete profile and employment details.

**What it includes**:

- **Personal Details**: Phone, address, date of birth, nationality
- **Emergency Contact**: Emergency contact name, phone, and relationship
- **Contract Management**: Upload and manage employment contracts
- **Location History**: Track location assignments over time
- **Holiday Allowance**: Manage holiday days and calculations

**When to do this**: After creating the user, when ready to set up detailed employment information.

### Why This Two-Step Design?

#### **✅ Separation of Concerns**

- **Creation**: Basic system access (who, authentication, roles)
- **Configuration**: Detailed employment profile (personal info, contracts, skills)

#### **✅ Flexibility**

- Can create a user without configuring detailed profile immediately
- Can update profile information without affecting authentication
- Different users might handle creation vs. configuration

#### **✅ Data Integrity**

- Basic user info rarely changes (email, roles)
- Profile information changes more frequently
- Separate validation rules for each

#### **✅ Role Separation**

- **User Creation**: Usually handled by admins/HR
- **User Configuration**: Can be handled by HR or the user themselves

### Practical Example: New Employee Setup

Let's walk through setting up a new employee:

#### **Step 1: Create User** (Admin/HR does this)

```
User: "Sarah Johnson"
Email: "sarah.j@company.com"
Password: "********"
Roles: Location Manager
Company: Coffee Express Ltd.
```

#### **Step 2: Configure User** (HR/User does this)

```
Phone: "+1 234-567-8901"
Address: "123 Main Street, Downtown"
Date of Birth: "1990-05-15"
Nationality: "Canadian"
Emergency Contact: { name: "John Johnson", phone: "+1 234-567-8902", relationship: "Spouse" }
```

#### **Result**

- **Creation**: Establishes the user as a system member with basic access
- **Configuration**: Sets up complete employment profile and details

### User Configuration Access

User configuration is accessed through:

- **User Management** → Select User → **Configuration** tab
- **Personal Profile** → **Configuration** (for own profile)

**Note**: Access to user configuration is controlled by granular permissions:

- `users.configuration.view` - View user configuration
- `users.configuration.overview` - Access user overview
- `users.configuration.contract` - Manage user contracts
- `users.configuration.location` - Manage user location assignments

## System-Level Users

### 1. Super Administrator

This is the highest level of access in the system.

**Characteristics:**

- Can access and manage all companies
- Can switch between different companies
- Has all permissions automatically
- Cannot have permissions revoked
- Typically assigned to system maintainers or platform owners

**Typical Tasks:**

- Creating new companies
- Managing company administrators
- System-wide configuration
- Access to all features across all companies

### 2. Company Administrator

The highest level of access within a specific company.

**Characteristics:**

- Full access within their own company
- Cannot access other companies' data
- Has all company-level permissions
- Can manage all aspects of their company
- Cannot switch between companies

**Typical Tasks:**

- Managing company users
- Setting up locations
- Creating custom roles
- Managing company settings

## Permission-Based Users

These users are defined by their assigned permissions. Here are some common examples:

### 1. Location Manager

**Typical Permissions:**

- `locations.configuration.manage`
- `locations.configuration.assign_shifts`
- `users.configuration.location`
- `schedules.view.all`
- `schedules.create`
- `schedules.update`

**Typical Tasks:**

- Managing specific locations
- Creating and updating schedules
- Assigning staff to shifts
- Viewing all schedules for their location

### 2. Schedule Manager

**Typical Permissions:**

- `schedules.create`
- `schedules.read`
- `schedules.update`
- `schedules.view.all`
- `schedules.assignment.manage`

**Typical Tasks:**

- Creating schedules
- Managing shift assignments
- Updating existing schedules
- Viewing all schedule information

### 3. Staff Member

**Typical Permissions:**

- `schedules.view.own`
- `users.holiday.request`
- `tasks.read`

**Typical Tasks:**

- Viewing their own schedule
- Submitting holiday requests
- Viewing assigned tasks
- Updating their profile

### 4. HR Manager

**Typical Permissions:**

- `users.create`
- `users.read`
- `users.update`
- `users.configuration.contract`
- `users.holiday.approve`
- `users.holiday.allowance.manage`

**Typical Tasks:**

- Managing employee information
- Handling contracts
- Approving holiday requests
- Managing holiday allowances

## Important Notes

1. **Flexible Permissions:**

   - These are just common examples
   - Actual permissions can be customized
   - Users can have any combination of permissions

2. **Multiple Roles:**

   - Users can have multiple sets of permissions
   - Permissions can be added or removed as needed
   - Roles can be customized for specific needs

3. **Access Levels:**
   - All permissions are company-specific (except Super Admin)
   - Users can only access their assigned company
   - Permissions don't cross company boundaries

## Support

For questions about user types or to request permission changes, contact your system administrator.
