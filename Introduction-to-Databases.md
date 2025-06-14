# Introduction to Databases – README

## Q1) Problem Statement

There can be multiple **customers**, each capable of placing multiple **orders** on the site.  
Every order is assigned to a **single salesperson**, but each **salesperson can manage multiple orders** from different customers.

---

## Q2) Design Schema

### Tables Overview

- **`customers`**: Stores customer details such as name and contact information.
- **`salespersons`**: Stores information about the sales representatives handling orders (e.g., name, contact).
- **`orders`**: Represents individual orders. Each is linked to a customer and a salesperson and has a date/time.
- **`products`**: Contains product catalog entries — name, price, and description.
- **`order_items`**: A bridge table that records which products (and how many) were ordered in each order. Also stores price at time of purchase.

### ER Diagram

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

---

## Q4) Insert Sample Data

### Customers

<img width="358" alt="Customers" src="https://github.com/user-attachments/assets/761d100b-ba24-4e3c-aeeb-1c20b36a181e" />

---

### Salespersons

<img width="370" alt="Salespersons" src="https://github.com/user-attachments/assets/509c46bc-9319-4e92-adec-3f3efd8e9009" />

---

### Products

<img width="442" alt="Products" src="https://github.com/user-attachments/assets/52ea6b64-53fc-491c-906b-4514fbf781e9" />

---

### Orders

<img width="477" alt="Orders" src="https://github.com/user-attachments/assets/793feb9d-46e9-4672-bfef-d90fe173dbdc" />

---

### Order Items

<img width="617" alt="Order Items" src="https://github.com/user-attachments/assets/46dda891-a077-476e-9d6b-ea8053c86f72" />

## Q5) Find the sales person have multiple orders.
### Query

![Query - Find Salespersons with Multiple Orders](https://github.com/user-attachments/assets/2fcee486-2fd4-42fc-8d1a-9f15b84fb86f)

### Output

![Output - Salespersons with Multiple Orders](https://github.com/user-attachments/assets/ad71c528-a925-4b5b-8e4f-4f3f9376a97b)
