# Odoo x Amalthea, IIT GN Hackathon 2025

Smart Expense Management & Approval System built with the **MERN Stack** for **Odoo x Amalthea, IIT Gandhinagar Hackathon 2025**.  
This project automates and streamlines the **expense reimbursement process** with flexible approval workflows, conditional rules, OCR-powered receipt scanning, and real-time currency-aware expense tracking.

---

## 🚩 Problem Statement
Companies often struggle with manual expense reimbursement processes that are:
- Time-consuming
- Error-prone
- Lacking transparency

### Challenges we solve:
- Define **approval flows** based on thresholds.
- Manage **multi-level approvals** (Manager → Finance → Director).
- Support **flexible & conditional approval rules**.
- Provide **transparent tracking** for employees and managers.

---

## 🔑 Core Features

### 🔐 Authentication & User Management
- Sign up → Auto-create **Company** & **Admin** (default currency based on country).
- Admin can create employees/managers, assign/change roles, and define manager relationships.

### 💸 Expense Submission (Employee Role)
- Submit expense claims (amount, category, description, date).
- Supports **multi-currency expenses** (conversion handled via API).
- View expense history (Approved / Rejected).

### ✅ Approval Workflow (Manager/Admin Role)
- Multi-level approval flow (Manager → Finance → Director).
- Sequence-based approvals: expense moves forward only if the current approver approves.
- Approvers can **approve/reject with comments**.

### 🔄 Conditional Approval Flow
- **Percentage rule** → e.g., 60% approvers must approve.
- **Specific approver rule** → e.g., CFO auto-approval.
- **Hybrid rule** → combine both.

### 👥 Role Permissions
- **Admin** → Manage company, users, approval rules, override approvals.
- **Manager** → Approve/reject, view team expenses, escalate as per rules.
- **Employee** → Submit expenses, view their own status/history.

### 📷 OCR for Receipts
- Scan receipts → OCR auto-extracts amount, date, description, and merchant name.

---

## ⚙️ Tech Stack
- **MongoDB** – Database
- **Express.js** – Backend framework
- **React.js** – Frontend
- **Node.js** – Server runtime
- **APIs**:
  - Country & Currency → [REST Countries API](https://restcountries.com/v3.1/all?fields=name,currencies)  
  - Currency Conversion → [ExchangeRate API](https://api.exchangerate-api.com/v4/latest/USD)
- **OCR** → Tesseract.js / EasyOCR

---

## 🖼️ Mockups
[Excalidraw Mockup Link](https://link.excalidraw.com/l/65VNwvy7c4X/4WSLZDTrhkA)

---

## 🚀 Quick Start (Development)

### 1. Clone the repo
```bash
git clone https://github.com/<your-org>/mern-expenseflow-hackathon-2025.git
cd mern-expenseflow-hackathon-2025
