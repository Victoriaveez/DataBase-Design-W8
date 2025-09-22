# DataBase-Design-W8
# E-commerce Store Database

This project is a MySQL database for a simple E-commerce Store. It includes users, products, orders, payments, and more.

## 📌 Features

- Users and addresses
- Product categories and listings
- Orders with multiple items
- Payment tracking

## 🗂️ Tables

- `users`
- `addresses`
- `categories`
- `products`
- `orders`
- `order_items`
- `payments`

## 🔗 Relationships

- One-to-Many: users → addresses, users → orders
- Many-to-One: products → categories
- Many-to-Many: orders ↔ products (via order_items)
- One-to-One: orders → payments

## ▶️ How to Use

1. Open MySQL Workbench or CLI.
2. Run the SQL script: `ecommerce_store.sql`
3. The script will:
   - Create the database and tables
   - Insert sample data (users, products, orders, etc.)

## ✅ Sample Query

```sql
SELECT u.name, o.order_id, o.status
FROM users u
JOIN orders o ON u.user_id = o.user_id;

