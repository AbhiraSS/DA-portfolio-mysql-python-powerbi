# Customer Shopping Behavior Analysis

An end-to-end data analytics project that studies **3,900 retail purchases** to understand how customers spend, which segments drive revenue, which products perform best, and how subscriptions and discounts affect buying behavior.

**Tools:** Python (pandas) · MySQL · Power BI

---

## Table of Contents

1. [Business Problem](#business-problem)
2. [Dataset](#dataset)
3. [Project Workflow](#project-workflow)
4. [Key Findings](#key-findings)
5. [Dashboard](#dashboard)
6. [Business Recommendations](#business-recommendations)
7. [Repository Structure](#repository-structure)
8. [How to Run](#how-to-run)
9. [Author](#author)

---

## Business Problem

A retail company wants to improve sales, customer satisfaction and long-term loyalty. Management has noticed shifts in purchasing patterns across demographics, product categories and sales channels, and wants to know which factors (discounts, reviews, seasons, payment preferences) drive purchase decisions and repeat buying.

The central question:

> How can the company use consumer shopping data to spot trends, strengthen customer engagement, and optimize its marketing and product strategies?

---

## Dataset

| Property | Value |
|---|---|
| Rows | 3,900 |
| Columns | 18 |
| Missing values | 37 (Review Rating) |

**Feature groups**

- **Demographics:** age, gender, location, subscription status
- **Purchase details:** item purchased, category, purchase amount, season, size, color
- **Shopping behavior:** discount applied, promo code used, previous purchases, frequency of purchases, review rating, shipping type, payment method

---

## Project Workflow

### 1. Data preparation in Python

- Loaded the dataset with pandas and explored it with `df.info()` and `df.describe()`
- Filled the 37 missing review ratings with the **median rating of each product category**
- Renamed columns to `snake_case`
- Engineered new features: `age_group` (binned ages) and `purchase_frequency_days`
- Found that `discount_applied` and `promo_code_used` carried the same information, so `promo_code_used` was dropped
- Loaded the cleaned DataFrame into a **MySQL** database

### 2. Analysis in MySQL

Ten business questions were answered with SQL:

| # | Question |
|---|---|
| 1 | Revenue by gender |
| 2 | High-spending customers who used a discount |
| 3 | Top 5 products by average rating |
| 4 | Average purchase amount: Standard vs. Express shipping |
| 5 | Subscribers vs. non-subscribers: spend and revenue |
| 6 | Top 5 discount-dependent products |
| 7 | Customer segmentation (New / Returning / Loyal) |
| 8 | Top 3 products per category |
| 9 | Are repeat buyers (more than 5 purchases) more likely to subscribe? |
| 10 | Revenue by age group |

### 3. Visualization in Power BI

An interactive dashboard with KPI cards, subscription split, sales and revenue by category, sales and revenue by age group, purchase amount by season, and slicers for category and shipping type.

---

## Key Findings

- **Gender:** Male customers generated **$157,890** versus **$75,191** from female customers, roughly 2.1 times as much.
- **Loyalty:** 3,116 customers are Loyal, 701 Returning and 83 New.
- **Repeat buyers:** Of customers with more than 5 purchases, 958 are subscribers and 2,518 are not.
- **Subscriptions:** Average spend is almost identical (**$59.49** for subscribers, **$59.87** for non-subscribers), so subscription value has to come from retention, frequency or perks rather than higher basket size.
- **Discounts:** Hat (50.00%), Sneakers (49.66%), Coat (49.07%), Sweater (48.17%) and Pants (47.37%) have the highest share of discounted purchases. 839 discount users still spent above the average purchase amount.
- **Ratings:** Highest-rated items are Gloves (3.86), Sandals (3.84), Boots (3.82), Hat (3.80) and Skirt (3.78).
- **Shipping:** Express orders average **$60.48** versus **$58.46** for Standard.
- **Age groups:** Young Adults contribute the most revenue ($62,143), followed by Middle-aged ($59,197), Adult ($55,978) and Senior ($55,763).
- **Categories:** Clothing and Accessories lead in both sales and revenue.

---

## Dashboard

![Customer Behaviour Dashboard](images/dashboard.png)


---

## Business Recommendations

1. **Boost subscriptions:** Test exclusive member benefits and perks, especially for the 2,518 repeat buyers who are not yet subscribed.
2. **Reward loyalty:** Build loyalty programs that move Returning customers into the Loyal segment.
3. **Review discount policy:** Balance the sales lift from discounts against margins, for example with minimum spend thresholds.
4. **Position top products:** Feature top-rated and best-selling items in campaigns and bundles.
5. **Target marketing:** Focus on the highest-revenue age groups and on express-shipping customers.

--<img width="1302" height="746" alt="Screenshot 2026-11-26 122302" src="https://github.com/user-attachments/assets/3f5c1bbe-04be-48d6-a3a0-0939fe3031f7" />


**<Your Name>**
[GitHub](https://github.com/<your-username>) · [LinkedIn](https://www.linkedin.com/in/<your-profile>)
