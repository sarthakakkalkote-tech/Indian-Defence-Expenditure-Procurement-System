# India Defence Expenditure & Procurement Management System (IDE-PMS)

An integrated, normalized Relational Database Management System (DBMS) and interactive analytics suite engineered to audit, analyze, and manage India's national defence budget outlays, tripartite expenditures, capital procurement contracts, and strategic asset inductions from 1947 to 2026.

---

## 📌 Project Overview

Managing sovereign military expenditures involves tracking three competing dimensions:
1. **Capital Acquisitions:** Hardware modernization, naval warships, fighter squadrons, and standoff weapons.
2. **Revenue Expenditures:** Day-to-day operating overhead, stores, ammunition restocking, and active troop pay.
3. **Defence Pensions:** Long-term personnel entitlements under One Rank One Pension (OROP) schemes.

**IDE-PMS** provides a structured 3NF/BCNF relational architecture that eliminates spreadsheet fragmentation, prevents contractor/vendor anomalies, enforces referential integrity constraints, and provides a built-in SQL query engine for real-time relational joins and aggregations.

---

## 🏗️ Relational Database Schema & Architecture

The database model consists of **6 normalized entities** designed up to **Third Normal Form (3NF) and Boyce-Codd Normal Form (BCNF)**:

```text
[Services] (1) <────── assigned ────── (N) [ProcurementContracts] (1) <── supplies ── (N) [CapitalAssets]
     ^                                              ^
     |                                              |
    (1)                                            (1)
     |                                              |
[Allocations]                                   [Vendors]

[AuditLogs] (Autonomous trigger logging table)
