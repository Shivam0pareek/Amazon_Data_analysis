# 📊 Amazon Brazil Market Analysis — SQL Project for Amazon India

## 📝 Project Overview

This project involves analyzing **Amazon Brazil’s e-commerce data** to extract key insights that can be leveraged by **Amazon India** to improve operations, customer experience, and business strategies.

The data covers multiple domains such as customers, orders, sellers, payments, and products. The analysis is divided into three main stages:

- ✅ Basic SQL Queries
- 🔁 Joins & Aggregations
- 🧠 Window Functions & CTEs

---

## 🎯 Objectives

- Identify **customer behavior**, **sales trends**, and **payment preferences**
- Understand **product-level performance** and **category-wise revenue**
- Build **customer segmentations** for loyalty programs
- Provide data-driven insights to improve business operations

---

## 🧱 Database Schema

The dataset includes 7 core tables:

| Table Name      | Description                                                  |
|------------------|--------------------------------------------------------------|
| `customers`      | Customer information including location and unique ID       |
| `orders`         | Order details, status, and purchase timestamp               |
| `order_items`    | Order-specific product details and seller info              |
| `products`       | Product metadata including category, name, and pricing      |
| `sellers`        | Seller information and their locations                      |
| `payments`       | Payment types and their transaction values                  |
| `geolocation`    | (Optional) Geo info for customer delivery mapping           |

### Relationships

- `orders.customer_id` → `customers.customer_id`
- `order_items.order_id` → `orders.order_id`
- `order_items.product_id` → `products.product_id`
- `order_items.seller_id` → `sellers.seller_id`
- `payments.order_id` → `orders.order_id`

---

## 🛠️ Setup Instructions

### 1. PostgreSQL Environment

- Install and launch **PostgreSQL** and **pgAdmin**
- Create database:
  ```sql
  CREATE DATABASE amazon_analysis;
