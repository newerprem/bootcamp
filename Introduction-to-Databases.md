# Introduction to Databases – README

## Q1) Problem Statement

There can be multiple customers who place multiple orders on the site.  
Each order is handled by a **single salesperson**, but each **salesperson can handle multiple orders** from different customers.

---

## Q2) Design Schema

**Tables:**

- `customers`: Stores customer information.
- `salespersons`: Stores salesperson information.
- `orders`: Stores order records linked to both customers and salespersons.

**Database creation command**
<img width="338" alt="Image" src="https://github.com/user-attachments/assets/9eee4b7c-8b39-4ce4-a53b-ddf17a9e5d4d" />
