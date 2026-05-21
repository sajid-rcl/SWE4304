# Online Store Management System

## Scenario

An online retail company needs a database system to manage customers, products, orders, deliveries, and payments. The system should help staff track customer purchases, monitor stock, and manage order processing efficiently.

The system should support:
- Managing customer accounts
- Managing products and categories
- Recording customer orders
- Tracking payments
- Managing deliveries
- Monitoring stock availability

---

# Candidate Entities

- Customer
- Order
- Product
- Payment
- Delivery
- Category
- OrderItem

---

# Example Tables and Sample Data

## Customers

| customer_id | customer_name | email | phone |
|---|---|---|---|
| C001 | Ahmed Ali | ahmed@email.com | 07123456789 |
| C002 | Sarah Khan | sarah@email.com | 07987654321 |

---

## Products

| product_id | product_name | price | stock_quantity |
|---|---|---|---|
| P001 | Wireless Mouse | 25.99 | 40 |
| P002 | Mechanical Keyboard | 79.99 | 15 |

---

## Categories

| category_id | category_name |
|---|---|
| CAT001 | Computer Accessories |
| CAT002 | Office Equipment |

---

## Orders

| order_id | order_date | customer_id | total_amount |
|---|---|---|---|
| O001 | 2026-06-10 | C001 | 105.98 |
| O002 | 2026-06-12 | C002 | 79.99 |

---

## OrderItems

| order_item_id | order_id | product_id | quantity |
|---|---|---|---|
| OI001 | O001 | P001 | 2 |
| OI002 | O002 | P002 | 1 |

---

## Payments

| payment_id | payment_method | payment_date | order_id |
|---|---|---|---|
| PAY001 | Credit Card | 2026-06-10 | O001 |
| PAY002 | PayPal | 2026-06-12 | O002 |

---

## Deliveries

| delivery_id | delivery_address | delivery_status | order_id |
|---|---|---|---|
| D001 | Manchester, UK | Shipped | O001 |
| D002 | London, UK | Processing | O002 |

---

# Example Relationships

- Customer places Order
- Order contains OrderItem
- Product appears in OrderItem
- Order has Payment
- Order has Delivery
- Product belongs to Category

---

# Example Assumptions

1. Each customer can place multiple orders.
2. Each order belongs to one customer.
3. An order can contain multiple products.
4. Each payment is linked to one order.
5. Each delivery record belongs to one order.

---

# Example Scope Statement

## In Scope
- Customer management
- Product management
- Order processing
- Payment tracking
- Delivery tracking

## Out of Scope
- Supplier management
- Warehouse automation
- Refund processing
- International shipping
