---
layout: post
title:  "Confident Ruby"
date:   2014-03-09 22:51:42
categories: [programming, ruby, reading]
---

### Collecting Input
  1. Identify the messages
  2. Identify the role (receiver) which correspond to those messages
  3. Ensure the method’s logic receives objects which can play
  those roles

  #### description
  ```
    1. Parse the purchase records from the CSV contained in a provided IO object.
    2. For each purchase record, use the record’s email address to get the associated customer record, or, if the email hasn’t been seen before, create a new customer record in our system.
    3. Use the legacy record’s product ID to find or create a product record in our system.
    4. Add the product to the customer record’s list of purchases.
    5. Notify the customer of the new location where they can download their files and update their account info.
    6. Log the successful import of the purchase record.
  ```
  #### Identify the message
  ```ruby
    1. #parse_legacy_purchase_records.
    2. For #each purchase record, use the record’s #email_address. to
#get_customer.
    3. Use the record’s product_id to #get_product.
    4. #add_purchased_product to the customer record.
    5. #notify_of_files_available for the purchased product.
    6. #log_successful_import of the product record.
  ```
  #### Identify the role
  ```
  1. legacy_data_parser.parse_purchase_records.
  2. Forpurchase_list.eachpurchase_record,usepurchase_record.email_address
  to customer_list.get_customer.
  3. Usethepurchase_record.product_idtoproduct_inventory.get_product.
  4. customer.add_purchased_product.
  5. customer.notify_of_files_available for the product.
  6. self.log_successful_import of the purchase_record.
  ```
  #### Converting to real code

### Performing Task

### Delivering output

### Handling failures

