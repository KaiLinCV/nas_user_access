📘 [English](README.md) | 📙 [中文](README_zh.md)

# 💽 Synology NAS – User Access Simulation Lab

This project simulates a small business network setup where users are divided into groups based on their job roles — such as Development, Finance, and General Staff. My goal with this lab was to demonstrate user and group management, implement secure password policies, and enforce the Principle of Least Privilege when configuring access to shared folders on a Synology NAS. It also served as hands-on practice for me to become more familiar with real-world NAS setup and administration tasks.

---

## 🔍 Overview

The following are the steps and concepts I used to replicate what a system administrator would do:
- Manage users across different departments.
- Apply the **Principle of Least Privilege** to folder access.
- Protect admin-only folders (e.g., `MyStorage`, `Workspace`).
- Enforce **secure password policies** to strengthen network access control.

---

## 🎯 Key Objectives

- Practice setting up and organizing **users and groups** using Synology DSM.
- Configure **password rules** (complexity, length, exclusions).
- Test file access with restricted permissions per group.
- Get hands-on experience with real-world system administration tasks and become more familiar with user policy management and access control processes.

---

## 👤 User and Group Setup

In this simulation lab, I created three different users, each assigned to their own group to represent different roles within an organization. I also use a main admin account for both this lab and my personal NAS access.
**Users:**
- `DevUser`
- `FinanceUser`
- `RegularUser`

**Groups:**
- `Dev`
- `Finance`
- `users` (Synology's default group)

**Admin Account:**
- `kailinc` (admin)

📷 Screenshots:
![Users](./screenshots/Users.png)
![Groups](./screenshots/Groups.png)

---

## 🔐 Password Policy

**Enforced Rules:**
- Minimum length: 8 characters
- Must include mixed case, numbers, and symbols
- Cannot include the user's name or description

📷 Screenshots:
![PasswordSettings](./screenshots/PasswordSettings.png)
![TestUsers_Pass](./screenshots/TestUsers_Pass.png)

---

## 📁 Folder Access by User Role

| User          | Group     | Accessible Folders             | Notes                                |
|---------------|-----------|--------------------------------|----------------------------------------|
| `RegularUser` | `users`   | `PublicFolder` only            | No access to Dev or Finance folders   |
| `FinanceUser` | `Finance` | `PublicFolder`, `FinanceFolder`| Access limited to finance-related data|
| `DevUser`     | `Dev`     | `PublicFolder`, `DevFolder`    | Access limited to dev-related data    |

🎥 Video Walkthroughs:
- General Staff User Folder Access

https://github.com/user-attachments/assets/efd73783-7f67-4bc9-8ed7-a2b992ae486f

- Finance User Folder Access

https://github.com/user-attachments/assets/9e257319-ac77-4cc8-bf45-9eabc6ab3def

- Dev User Folder Access

https://github.com/user-attachments/assets/7cb5c6f3-b050-496d-9e77-29a85c857909




---

## 🧠 Summary & What I Learned

This simulation helped me:
- Get hands-on experience managing **user roles and permissions**.
- Understand **password hardening** in a production-like environment.
- Reinforce core concepts of **least privilege** and **role-based access control**.
- Better prepare for real-world **System Administrator** responsibilities.
