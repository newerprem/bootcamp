# 📘 Introduction to Databases – README

## Q1) Problem Statement

There can be multiple **customers** who place multiple **orders** on the site.  
Each order is handled by a **single salesperson**, but each **salesperson can handle multiple orders** from different customers.

---

## Q2) Design Schema

### Tables:

- `customers`: Stores customer details like name, contact, and address.
- `salespersons`: Contains information about sales representatives handling orders, such as name, region, and contact details.
- `orders`: Stores individual customer orders. Each order is linked to a specific customer and assigned to one salesperson. Also records the date/time of the order.
- `products`: Represents the product catalog including product names, prices, and descriptions.
- `order_items`: Tracks which products are part of which order, including quantity and per-item price at the time of purchase. This enables detailed order history and billing.

### Database Creation Command

![Database Creation](https://github.com/user-attachments/assets/1c007aad-c686-49fb-a26b-946c6adc2cc5)

---

## Q3) Create Tables

### Customers Table

![Customers Table](https://github.com/user-attachments/assets/bf90ea18-0c99-438e-8912-82ddefb82eb3)

---

### Salespersons Table

![Salespersons Table](https://github.com/user-attachments/assets/72ae74bf-26f4-4089-947b-acf20e6580c1)

---

### Orders Table

![Orders Table](https://github.com/user-attachments/assets/fdd8d441-2671-4ffa-8099-b9d1566dc042)

---

### Products Table

![Products Table](https://github.com/user-attachments/assets/9385dd32-6eed-44a6-9bfb-f8fabbf4047f)

---

### Order Items Table

![Order Items Table](https://github.com/user-attachments/assets/11e907f4-cbd8-4c6d-a3e4-e0afceb74461)
