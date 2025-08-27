---
layout: default
title: Roles and Permissions
description: Understanding the permission-based access control system
---

# Roles and Permissions System

## Overview

Our system uses a flexible permission-based approach rather than fixed roles. This means access to features is controlled by specific permissions rather than traditional role titles.

## Built-in Roles

The system has only two fixed roles:

1. **Super Administrator**

   - Has complete system access
   - Can manage all companies
   - Can switch between different companies
   - Cannot be restricted

2. **Administrator**
   - Has complete access within their company
   - Can only manage their own company
   - Cannot access other companies' data

## Custom Roles

Instead of using predefined roles like "manager" or "staff", our system allows companies to create custom roles by combining different permissions. This provides maximum flexibility for each company's unique needs.

### How Custom Roles Work

1. **Creating a Role**:

   - Give the role a name
   - Select the permissions for this role
   - Assign the role to users

2. **Example Custom Roles**:
   - "Schedule Manager" - only schedule-related permissions
   - "Location Manager" - location and staff management permissions
   - "Staff Member" - basic access permissions

## Available Permissions

Our system includes the following permission categories:

### User Management

- `users.create` - Create new users
- `users.read` - View user list
- `users.update` - Update user information
- `users.delete` - Remove users from the system
- `users.configuration.view` - View user configuration
- `users.configuration.overview` - Access user overview
- `users.configuration.contract` - Manage user contracts
- `users.configuration.location` - Manage user location assignments
- `users.configuration.schedule` - Manage user schedules

### Location Management

- `locations.create` - Create new locations
- `locations.read` - View location list
- `locations.update` - Update location information
- `locations.delete` - Remove locations
- `locations.assign.single` - Assign single location to users
- `locations.assign.multiple` - Assign multiple locations to users
- `locations.configuration.manage` - Manage location settings
- `locations.configuration.view` - View location configuration
- `locations.configuration.assign_shifts` - Assign shifts at locations

### Schedule Management

- `schedules.create` - Create new schedules
- `schedules.read` - View schedule list
- `schedules.update` - Update schedules
- `schedules.delete` - Remove schedules
- `schedules.view.all` - View all schedules
- `schedules.view.own` - View own schedules only
- `schedules.assignment.manage` - Manage schedule assignments

### Holiday Management

- `users.holiday.request` - Submit holiday requests
- `users.holiday.approve` - Approve holiday requests
- `users.holiday.view` - View holiday information
- `users.holiday.allowance.manage` - Manage holiday allowances
- `users.holiday.allowance.view` - View holiday allowances

### Task Management

- `tasks.create` - Create new tasks
- `tasks.read` - View task list
- `tasks.update` - Update tasks
- `tasks.delete` - Remove tasks
- `tasks.approve` - Approve tasks
- `tasks.assign` - Assign tasks to users

### Reports

- `reports.read` - Access Reports Page
- `reports.worked-hours` - Generate Worked Hours Reports
- `reports.view_dynamic_data` - View Report Template Analytics

### Report Templates

- `templates.create` - Create new report templates
- `templates.read` - View report template list
- `templates.update` - Modify existing report templates
- `templates.delete` - Remove report templates
- `templates.assign` - Assign report templates to users
- `templates.analytics.view` - View report template analytics dashboards
- `templates.analytics.export` - Export report template data (PDF, Excel, JSON)

### Role Management

- `roles.create` - Create new roles
- `roles.read` - View role list
- `roles.update` - Update roles
- `roles.delete` - Remove roles

### Settings

- `settings.read` - View system settings

## Benefits of This Approach

1. **Flexibility**:

   - Create roles that exactly match your needs
   - Easily modify permissions as responsibilities change
   - No limitations from predefined roles

2. **Security**:

   - Precise control over what users can do
   - Easy to audit who has what permissions
   - Simple to adjust access when needed

3. **Scalability**:
   - New permissions can be added easily
   - Roles can be updated instantly
   - Works for any organization structure

## Support

For questions about roles and permissions, contact your system administrator.
