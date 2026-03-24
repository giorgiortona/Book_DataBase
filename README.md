# Book_DataBase
# 📚 Bookstore Database (Microsoft Access)

This project is a relational database developed in Microsoft Access to manage the main operations of a bookstore.

## 📌 Overview
The system supports:
- Book management
- Customer management
- Supplier management
- Sales (Orders)
- Purchases
- Inventory tracking
- Data analysis through queries

The database is designed to be simple, consistent and user-friendly.

---

## 🧱 Database Structure

Main entities:
- Book
- Customer
- Supplier
- Publisher
- Category
- Order and Order_line
- Purchase and Purchase_line
- Inventory
- Store

Relationships are implemented using primary and foreign keys, ensuring referential integrity.  
Many-to-many relationships are resolved through intermediate tables such as **Order_line** and **Purchase_line**.

---

## ⚙️ Core Features

### 🛒 Sales Management
- Orders are managed through **F_Order**
- Each order can contain multiple books (Order_line)
- Unit price is automatically retrieved from the Book table
- Orders can be completed using a button

### 📦 Purchase Management
- Purchases are managed through **F_Purchase**
- Each purchase includes multiple items (Purchase_line)
- Unit cost can be automatically suggested from book data

### 📊 Inventory Management
- Inventory shows available stock for each book
- Stock is automatically updated:
  - when an order is completed → stock decreases
  - when a purchase is completed → stock increases

---

## 🧠 Business Logic

The system includes several automated rules:

- **Order total calculation**

Total_list = sum of (Qty × Unit_price)
Total_paid = Total_list − Total_discount
Total_amount = sum of (Qty × Unit_cost)


- Orders cannot exceed available stock
- Line numbers in order and purchase lines are automatically generated
- Calculated values are not stored to avoid redundancy

---

## 🔍 Queries

The following queries are implemented:

- Orders per customer  
- Purchases per supplier  
- Bestseller by period  
- Inventory  
- Books to reorder  
- Price update by publisher  

These queries support both operational tasks and data analysis.

---

## 🖥️ User Interface

The database includes a user-friendly interface built with forms:

- F_Book  
- F_Customer  
- F_Supplier  
- F_Order (with Order_line subform)  
- F_Purchase (with Purchase_line subform)  
- F_Inventory  
- F_BestsellerPeriodo  
- F_Update_prices  

Features:
- Combo boxes hide technical IDs and show readable values
- Buttons automate actions (close order, update prices, etc.)
- Main menu (F_MenuPrincipale) allows easy navigation

---

## 🔐 Versions

Two versions of the database are provided:

- **DEV version**
- Full access to tables, queries and structure
- Used for development and testing

- **USER version**
- Restricted access
- Navigation pane hidden
- Users interact only through forms and buttons

This simulates a real-world business environment.

---

## 🚀 How to Use

1. Open the **USER version**
2. Use the main menu to navigate:
 - Sales
 - Purchases
 - Inventory
3. Insert data using forms
4. Complete orders or purchases to update inventory automatically

---

## 🛠️ Technologies Used

- Microsoft Access
- SQL (queries)
- VBA (automation and business logic)

---

## 📄 Project Purpose

This project demonstrates:
- correct database design (ER model → implementation)
- use of relational structures and integrity constraints
- automation of business processes
- creation of a simple but realistic database application

---

## 👨‍💻 Author

Giorgio Ortona
