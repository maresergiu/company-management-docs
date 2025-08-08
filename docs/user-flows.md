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
