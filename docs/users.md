---
layout: default
title: User Types
description: Common user roles and their responsibilities
---

# User Types and Their Roles

## Overview

In our platform, users are defined by their permissions rather than fixed roles. However, there are some common user types based on typical permission combinations.

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
