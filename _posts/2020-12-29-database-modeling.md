---
layout: post
title:  Database Modeling and Design
date:   2020-12-19 14:50:35 +0300
image:  '/assets/img/database.png'
tags:   [in_blog]
---

> Dimensional Modeling is a technique that making database simple and optimizes query performance.

---

## Background& Problem

A shipping company provides service to customers who want to sell their products and ship items to other customers.  The company needs a database design solution for their shipment invoice.

## Goal
The company needs a database design to store shipment invoice information containing an invoice number, shipping address, warehouse and customer name, etc.

For this design, I analyzed the company's information need for the invoice, broke them down into different tables to optimize query performance, and helped the company's business analyst access the data.

## Dimensional Modeling Technique

For this project, I used the **star schema** to design the database.
Star schema contains a deep and thin fact table stores the performance measurement result such as quantity and fee. Dimension tables stores descriptive context associated with the business process measurement.

---

## Design
I designed a fact table to store all foreign key that connects different dimensions and measurement facts. Each dimension table describes the "who, how, where" of the shipping process. For example, the customer dimension contains customer information, and the warehouse dimension includes information on the shipping address.

In addition, I use the mini-dimension and role-playing dimension technique to prevent dimensions from growing too big, which might decrease querying performance.



* **Mini Dimension**
The shipping company wants to analyze customer type frequently. I designed a customer-type mini-dimension that stores a subset of customer attributes changed or needed to be examined frequently. With customer type table, the business users easily analyze different customer size's service usage performance.

* **Role-playing dimension**
Since any customer may ship items to any other customer, I designed it as a role-playing dimension. Since the company services the group of customers, they can be both sender and receiver. For the date dimension, the company needs to track the shipment date, pick-up, and delivery date; I added three foreign keys in the fact table that connects to the date dimension.

![]({{site.baseurl}}/assets/img/database.png)

## Takeaway:
Before jumping into database design, it is critical to understand the business process and the business need. Determine line item that can reflect the process and store all information. With the right data in place and quick query performance, the business user can analyze data as need and improve decision making.



