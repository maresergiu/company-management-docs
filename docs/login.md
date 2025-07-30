---
layout: default
title: Login System Documentation
description: Secure access to the Company Management System with 2FA support
---

# Login System Documentation

## Overview

The login system provides secure access to the Company Management System with support for two-factor authentication (2FA). This document explains how the login process works.

## Login Process

### Step 1: Basic Login

1. Users enter their:

   - Email address
   - Password

2. The system validates:

   - Email format is correct
   - Password is at least 6 characters long

3. After successful validation:
   - If the user has 2FA enabled → Goes to Step 2
   - If no 2FA → Direct login to dashboard

### Step 2: Two-Factor Authentication (2FA) - If Enabled

1. System sends a verification code to user's email
2. User enters the 6-digit code
3. System verifies the code
4. Access granted upon successful verification

## After Login

The system automatically directs users to their appropriate dashboard based on their permissions:

1. **Super Administrators**:

   - Direct access to system dashboard
   - Can switch between different companies

2. **Regular Users**:
   - Directed to their company dashboard
   - Access based on their specific permissions

## Important Notes

- Automatic logout after 1 hour of inactivity
- "Forgot Password" option available on login screen
- Failed login attempts show clear error messages
- Users can enable/disable 2FA from their profile settings

## Security Features

- Email format validation
- Password strength requirements
- Two-factor authentication option
- Secure session management
- Permission-based access control

## Support

If you experience any issues logging in, please contact your system administrator.
