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

Stores customer account and contact information.

| customer_id | customer_name | email | phone |
|---|---|---|---|
| 1 | John Smith | john@email.com | 07123456789 |
| 2 | Emily Johnson | emily@email.com | 07987654321 |

---

## Products

Stores product details including price and stock quantity.

| product_id | product_name | price | stock_quantity | category_id |
|---|---|---|---|---|
| 1 | Wireless Mouse | 25.99 | 40 | 1 |
| 2 | Mechanical Keyboard | 79.99 | 15 | 1 |

---

## Categories

Stores product category information.

| category_id | category_name |
|---|---|
| 1 | Computer Accessories |
| 2 | Office Equipment |

---

## Orders

Stores customer order records and order totals.

| order_id | order_date | customer_id | total_amount |
|---|---|---|---|
| 1 | 2026-06-10 | 1 | 105.98 |
| 2 | 2026-06-12 | 2 | 79.99 |

---

## OrderItems

Stores the products included in each order and their quantities.

| order_item_id | order_id | product_id | quantity |
|---|---|---|---|
| 1 | 1 | 1 | 2 |
| 2 | 2 | 2 | 1 |

---

## Payments

Stores payment information related to customer orders.

| payment_id | payment_method | payment_date | order_id |
|---|---|---|---|
| 1 | Credit Card | 2026-06-10 | 1 |
| 2 | PayPal | 2026-06-12 | 2 |

---

## Deliveries

Stores delivery details and shipment status for orders.

| delivery_id | delivery_address | delivery_status | order_id |
|---|---|---|---|
| 1 | Manchester, UK | Shipped | 1 |
| 2 | London, UK | Processing | 2 |

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
