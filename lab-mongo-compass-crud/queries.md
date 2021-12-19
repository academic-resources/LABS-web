

# Answers

## 1. Find all the companies that include 'Facebook' on the **name** field.

 - **`query`**: {name: 'Facebook'}
 
 ## 2. Find all the companies which **category_code** is 'web'. Retrive only their `name` field:

 - **`query`**: {category_code: 'web'}
 - **`projection`**: {name: 1, _id: 0}

## 3. Find all the companies named "Twitter", and retrieve only their `name`, `category_code` and `founded_year` fields.

## 4. Find all the companies who have `web` as their **category_code**, but limit the search to 50 companies.

## 5. Find all the companies which **category_code** is 'enterprise' and have been founded in 2005. Retrieve only the `name`, `category_code` and `founded_year` fields.

## 6. Find all the companies that have been **founded** on the 2000 or have 20 **employees**. Sort them descendingly by their `number_of_employees`.

## 7. Find all the companies that do not include `web` nor `social` on their **category_code**. Limit the search to 20 documents and retrieve only their `name` and `category_code`.

## 8. Find all the companies that were not **founded** on 'June'. Skip the first 50 results and retrieve only the `founded_month` and `name` fields.

## 9. Find all the companies that have 50 employees, but do not correspond to the 'web' **category_code**. 

## 10. Find all the companies that have been founded on the 1st of the month, but does not have either 50 employees nor 'web' as their **category_code**. Retrieve only the `founded_day` and `name` and limit the search to 5 documents.

## 11. Find all the companies which the `price_amount` of the `acquisition` was **`40.000.000`**. Sort them by `name`.

## 12. Find all the companies that have been acquired on January of 2014. Retrieve only the `acquisition` and `name` fields.
