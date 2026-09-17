Online Bookstore SQL Analysis Project
Project Overview

The Online Bookstore SQL Analysis Project is a relational database project developed using PostgreSQL.

The purpose of this project is to analyze an online bookstore's data using SQL and answer practical business questions related to:

    📚 Books
    👥 Customers
    🛒 Orders
    💰 Revenue
    📦 Inventory
    📊 Sales
    👤 Customer purchasing behavior

The project uses three CSV datasets — Books, Customers, and Orders — which are connected through common columns such as Book_ID and Customer_ID.

This project demonstrates how SQL can be used to transform raw data into meaningful business information.
Project Objectives

The main objectives of this project are:

    Create a relational database for an online bookstore.
    Import raw CSV datasets into PostgreSQL.
    Establish relationships between different tables.
    Write SQL queries to retrieve and analyze data.
    Analyze books, customers, and orders.
    Calculate sales and revenue.
    Analyze inventory and remaining stock.
    Answer business-related questions using SQL.
    Practice both basic and advanced SQL concepts.

Dataset Description

The project contains three datasets.
1. Books Dataset

The Books table contains information about the books available in the bookstore.

Important fields include:

    Book_ID
    Title
    Author
    Genre
    Published_Year
    Price
    Stock

Purpose

This table can be used to analyze:

    Book genres
    Book prices
    Authors
    Publication years
    Available inventory
    Most and least expensive books
    Books with low stock

2. Customers Dataset

The Customers table contains information about bookstore customers.

Important fields include:

    Customer_ID
    Customer details
    City
    Country

Purpose

This table can be used to analyze:

    Customer locations
    Customers who place multiple orders
    Customer spending
    Purchasing behavior

3. Orders Dataset

The Orders table contains information about customer purchases.

Important fields include:

    Order_ID
    Customer_ID
    Book_ID
    Order_Date
    Quantity
    Total_Amount

Purpose

This table can be used to analyze:

    Orders
    Quantity of books sold
    Revenue
    Popular books
    Customer spending
    Sales by genre
    Sales by author

Database Relationships

The three tables are related using common columns.

                 ┌─────────────────┐
                 │    Customers    │
                 │─────────────────│
                 │ Customer_ID     │
                 └────────┬────────┘
                          │
                          │ Customer_ID
                          │
                          ▼
                 ┌─────────────────┐
                 │     Orders      │
                 │─────────────────│
                 │ Order_ID        │
                 │ Customer_ID     │
                 │ Book_ID         │
                 │ Quantity        │
                 │ Total_Amount    │
                 └────────┬────────┘
                          │
                          │ Book_ID
                          │
                          ▼
                 ┌─────────────────┐
                 │      Books      │
                 │─────────────────│
                 │ Book_ID         │
                 │ Title           │
                 │ Author          │
                 │ Genre           │
                 │ Price           │
                 │ Stock           │
                 └─────────────────┘


