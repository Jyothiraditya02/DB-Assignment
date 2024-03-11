# Database Schema Explanation

This document outlines the answers for the given questions regarding the database schema focusing on the relationship between `Product` and `Product_Category` entities.

## 1. Relationship between "Product" and "Product_Category"

The relationship between `Product` and `Product_Category` is a one-to-many relationship, where each product is linked to one product category, and each product category can have multiple products associated with it. This is represented in the database schema by a foreign key in the `Product` table (`category_id`) that references the primary key (`id`) of the `Product_Category` table.

## 2. Ensuring a Valid Category for Each Product

To ensure that each product has a valid category, the following constraints should be implemented:
- **Foreign Key Constraint**: The `category_id` in the `Product` table should have a foreign key constraint that references the `id` of the `Product_Category` table.
- **NOT NULL Constraint**: The `category_id` column should be set as NOT NULL to ensure that every product record includes a category.
- **Referential Integrity**: The database should enforce referential integrity to maintain consistent relationships between the two tables.
