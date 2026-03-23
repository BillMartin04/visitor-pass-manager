# Visitor Pass Manager
**Branding:** The Architect of a Smart City  
**Project Lead:** Bill Martin (Senior Business Consultant)

## Overview
A high-fidelity Visitor Management System built on the ServiceNow Vancouver/Washington D.C. platform. This application digitizes the guest lifecycle, providing secure, auditable access to corporate and urban facilities.

## Data Model (Relational Architecture)
This application utilizes a normalized 3-table structure:

1. **Visitor [x_555344_visitor_0_visitor]** (Parent/Master)
   - Stores core identity (First Name, Last Name, Email, Company).
   - Marked as **Extensible** for future "VIP" or "Contractor" sub-types.

2. **Visit Log [Planned]** (Child/Transactional)
   - One-to-Many relationship with the Visitor table.
   - Tracks individual entries, hosts, and timestamps.

3. **Badge [Planned]** (Security/Access)
   - One-to-One relationship with the Visit Log.
   - Manages physical or digital QR access keys.

## Technical Standards
- **Source Control:** GitHub integration for versioning.
- **Licensing:** Apache License 2.0.
- **Governance:** Managed via ServiceNow App Engine Studio (AES) submission pipelines.
