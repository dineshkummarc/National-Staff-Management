# National-Staff-Management-System-Backend-Laravel-Supabase-
# National Staff Management System

Laravel 12 REST API + React frontend that replaced a legacy PHP system to centralize
operations for a national organization, by Joven Andrei Lagahit (NythosX).

## Overview

A national organization was running on a legacy PHP system that had grown, patch by patch,
into something nobody fully trusted anymore. I rebuilt it on Laravel 12 with a React frontend,
modeling roles and permissions as first-class database records instead of translating the old
tangle of conditionals one to one — so the platform could scale to thousands of users without
falling apart under new requirements.

## Tech Stack

- Laravel 12 — REST API, policy-based role authorization
- React — SPA frontend with role-aware navigation
- Supabase — data layer
- Cloudways — hosting

## Core Features Owned

- Modeled roles and permissions as first-class database records, checked through Laravel's policy layer
- Scoped every API response to the requesting user's role at the query level, so a regional director can never pull another affiliate's member records by guessing an ID
- Indexed and paginated heavy list views to keep the dashboard responsive as member records scaled into the thousands
- Built a React frontend consuming a clean REST API, with navigation that reshapes itself per user role

## Impact

- 17 distinct user roles, each with a portal experience tailored to what that role actually needs to see
- 4,000+ users served across affiliate organizations
- Streamlined national staff operations by 40% through centralized management and automated role-based navigation
- Migrated from the legacy system without a single day of downtime

Full write-up: https://nythosx.pages.dev/projects/national-staff-management-system
