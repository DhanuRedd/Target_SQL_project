# Target_SQL_project : Query writing

## About company and data

Target is a globally renowned brand and a prominent retailer in the United States. Target makes itself a preferred shopping destination by offering outstanding value, inspiration, innovation and an exceptional guest experience that no other retailer can deliver.

This particular business case focuses on the operations of Target in Brazil and provides insightful information about 100,000 orders placed between 2016 and 2018. The dataset offers a comprehensive view of various dimensions including the order status, price, payment and freight performance, customer location, product attributes, and customer reviews.

🎯 Objective

By analyzing this extensive dataset, it becomes possible to gain valuable insights into Target's operations in Brazil. Shed light on various aspects of the business, such as order processing, pricing strategies, payment and shipping efficiency, customer demographics, product characteristics, and customer satisfaction levels.


## Datasets

### **Customers Table:**

| **Feature**                  | **Description**                                           |
|------------------------------|-----------------------------------------------------------|
| `customer_id`                | ID of the consumer who made the purchase                  |
| `customer_unique_id`         | Unique ID of the consumer                                 |
| `customer_zip_code_prefix`   | Zip Code of consumer’s location                           |
| `customer_city`              | Name of the City from where the order is made             |
| `customer_state`             | State Code from where the order is made (e.g., SP for São Paulo) |

### **Sellers Table:**

| **Feature**                  | **Description**                                           |
|------------------------------|-----------------------------------------------------------|
| `seller_id`                  | Unique ID of the seller registered                        |
| `seller_zip_code_prefix`     | Zip Code of the seller’s location                         |
| `seller_city`                | Name of the City of the seller                            |
| `seller_state`               | State Code (e.g., SP for São Paulo)                       |

### **Order Items Table:**

| **Feature**                  | **Description**                                           |
|------------------------------|-----------------------------------------------------------|
| `order_id`                   | Unique ID of the order made by the consumer               |
| `order_item_id`              | Unique ID given to each item ordered in the order         |
| `product_id`                 | Unique ID given to each product available on the site     |
| `seller_id`                  | Unique ID of the seller registered                        |
| `shipping_limit_date`        | Date before which the ordered product must be shipped     |
| `price`                      | Actual price of the products ordered                     |
| `freight_value`              | Delivery price from one point to another                 |

### **Geolocations Table:**

| **Feature**                  | **Description**                                           |
|------------------------------|-----------------------------------------------------------|
| `geolocation_zip_code_prefix`| First 5 digits of Zip Code                                |
| `geolocation_lat`            | Latitude                                                  |
| `geolocation_lng`            | Longitude                                                 |
| `geolocation_city`           | City                                                      |
| `geolocation_state`          | State                                                     |

### **Payments Table:**

| **Feature**                  | **Description**                                           |
|------------------------------|-----------------------------------------------------------|
| `order_id`                   | Unique ID of the order made by the consumer               |
| `payment_sequential`         | Sequence of payments made in case of EMI                  |
| `payment_type`               | Mode of payment used (e.g., Credit Card)                  |
| `payment_installments`       | Number of installments in case of EMI purchase            |
| `payment_value`              | Total amount paid for the purchase order                  |

### **Orders Table:**

| **Feature**                  | **Description**                                           |
|------------------------------|-----------------------------------------------------------|
| `order_id`                   | Unique ID of the order made by the consumer               |
| `customer_id`                | ID of the consumer who made the purchase                  |
| `order_status`               | Status of the order (e.g., delivered, shipped, etc.)      |
| `order_purchase_timestamp`   | Timestamp of the purchase                                 |
| `order_delivered_carrier_date`| Date carrier delivered the product                       |
| `order_delivered_customer_date`| Date customer received the product                     |
| `order_estimated_delivery_date`| Estimated delivery date of the product                  |

### **Reviews Table:**

| **Feature**                  | **Description**                                           |
|------------------------------|-----------------------------------------------------------|
| `review_id`                  | ID of the review given on the product                     |
| `order_id`                   | Unique ID of the order made by the consumer               |
| `review_score`               | Review score (1-5 scale)                                  |
| `review_comment_title`       | Title of the review                                       |
| `review_comment_message`     | Review comments posted by the consumer                    |
| `review_creation_date`       | Timestamp when the review was created                     |
| `review_answer_timestamp`    | Timestamp when the review was answered                    |

### **Products Table:**

| **Feature**                  | **Description**                                           |
|------------------------------|-----------------------------------------------------------|
| `product_id`                 | Unique ID of the product                                  |
| `product_category_name`      | Name of the product category                              |
| `product_name_lenght`        | Length of the product name string                         |
| `product_description_lenght` | Length of the product description                         |
| `product_photos_qty`         | Number of photos available for the product                |
| `product_weight_g`           | Weight of the product in grams                            |
| `product_length_cm`          | Length of the product in centimeters                      |
| `product_height_cm`          | Height of the product in centimeters                      |
| `product_width_cm`           | Width of the product in centimeters                       |

    
# Business Recommendations/Insights

1. Analyzed customer purchasing behavior across various states in Brazil.
2. Identified a **13,608.5%** increase in orders from **2016 to 2017** and a **19.75%** increase from **2017 to 2018**.
3. Utilized case statements to reveal peak order times: **afternoons (38%)**, **mornings and nights (28%)**, and **dawn (5%)**.
4. Observed that the number of orders generally increased year-over-year, with **August** having the highest monthly orders (**10,843**) across all years, except for **September** and **October**.
5. Noted that **São Paulo (SP)** consistently led in order counts across months.
6. Cost analysis showed a **137%** increase in 2018 compared to 2017 from **January to August**, indicating significant growth in orders and business operations.
7. **SP** had the highest total freight charges (**718,723.0**), while **Paraíba (PB)** and **Roraima (RR)** had the highest average freight prices due to lower order volumes.
8. The output generated **99,441 rows** due to a detailed delivery time analysis based on order IDs.
9. States like **Acre (AC)**, **Rondônia (RO)**, **Amazonas (AM)**, **Amapá (AP)**, and **Roraima (RR)** showed the highest average delivery delays, with **AC** averaging a **20-day** difference.
10. Analyzed order counts by payment type, revealing that credit cards dominated orders across months, while debit cards had the lowest volume.
