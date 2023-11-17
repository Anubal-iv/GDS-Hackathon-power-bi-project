Complete project video presentation: https://drive.google.com/file/d/1bv4fGKHHu5SgxG05YfO-VRO8eJfvJk4L/view?usp=sharing
**Project:** Generate Insights to Solve a Supply Chain Issue in FMCG Domain |
-------------------------------------------------------------------------------------------------------------------------------------------------
**Problem Statement:**
GDS Mart is a growing FMCG manufacturer headquartered in Gujarat, India. It is currently operational in three cities Surat, Ahmedabad and Vadodara. They want to expand to other metro/tier1 cities in the next 2 years.

GDS Mart is currently facing a problem where a few key customers have not extended the annual contract due to service issues. It is speculated that some of the essential products were either not delivered on time or not delivered in full over a continued period, which could have resulted in bad customer service. Management wants to fix this issue before expanding to other cities and requested their supply chain analytics team to track the ’On time’ and ‘In Full’ delivery service level for all the customers on a daily basis so that they can respond swiftly to these issues.

The Supply Chain team decided to use a standard approach to measure the service level in which they will measure ‘on-time delivery (OT) %’, ‘In-full delivery (IF) %’ and OnTime in full (OTIF) % of the customer orders on a daily basis against the target service level set for each customer.

Task:
Mr. Analyst is the data analyst in the supply chain team who joined GDS Mart recently. He has been briefed about the task in the stakeholder business review meeting. Now Imagine yourself as Mr. Analyst and play the role of the new data analyst who is excited to build this dashboard and perform the following task:
•	Create the metrics according to the metrics list( Below)
•	Create a dashboard according to the requirements provided by stakeholders in the business review meeting. You will be provided with the transcript of this business review meeting in the form of a comic.
•	Create relevant insights that are not provided in the metric list/stakeholder meeting.




Metrics List:

Sno	Measures	Abbreviation	Description	Table	
1	Total Order Lines		Count of all order lines in fact_orders table	fact_order_lines	
2	Line Fill Rate	LIFR %	Number of order lines shipped In Full Quantity / Total Order Lines	fact_order_lines	
3	Volume Fill Rate	VOFR %	Total Quantity shipped / Total Quantity Ordered	fact_order_lines	
4	Total Orders			fact_orders_aggregate	
5	On Time Delivery %	OT %	Number of orders delivered On Time / Total Number of Orders	fact_orders_aggregate	
6	In Full Delivery %	IF %	Number of orders delivered in Full quantity / Total Number of Orders	fact_orders_aggregate	
7	On Time In Full %	OTIF %	Number of orders delivered both IN Full & On Time / Total Number of Orders	fact_orders_aggregate	
8	On Time Target 		Average of On-Time Target 	dim_targets_orders	
9	In Full Target 		Average of In-Full Target	dim_targets_orders	
10	On Time In Full Target 		Average of OTIF Target	dim_targets_orders	
		  			

Meta Data:
We have provided 6 CSV files(folder attached):
1. dim_customers.csv
2. dim_products.csv
3. dim_date
4. dim_targets_orders
5. fact_order_lines.csv
6. fact_orders_aggregate.csv

Column Description for dim_customers:
1. customer_id: Unique ID is given to each customer
2. customer_name: Name of the customer
3. city: It is the city where the customer is present

Column Description for dim_products:
1. product_name: It is the name of the product
2. product_id: Unique ID is given to each of the products
3. category: It is the class to which the product belongs

Column Description for dim_date:
1. date: date at the daily level
2. mmm_yy: date at the monthly level
3. week_no: week number of the year as per the date column

Column Description for dim_targets_orders:
1.	customer_id: Unique ID that is given to each of the customers
2.	ontime_target %: Target assigned for Ontime % for a given customer
3.	infull_target %: Target assigned for infull % for a given customer
4.	otif_target %:   Target assigned for otif % for a given customer

Column Description for fact_order_lines:
1. order_id: Unique ID for each order the customer placed
2. order_placement_date: It is the date when the customer placed the order
3. customer_id: Unique ID that is given to each of the customers
4. product_id: Unique ID that is given to each of the products
5. order_qty: It is the number of products requested by the customer to be delivered
6. agreed_delivery_date: It is the date agreed between the customer and GDS Mart to deliver the products
7. actual_delivery_date: It is the actual date GDS Mart delivered the product to the customer
8. delivered_qty: It is the number of products that are actually delivered to the customer


Column Description for fact_orders_aggregate:
1. order_id: Unique ID for each order the customer placed
2. customer_id: Unique ID that is given to each of the customers
3. order_placement_date: It is the date when the customer placed the order
4. on_time: '1' denotes the order is delivered on time. '0' denotes the order is not delivered on time.
5. in_full: '1' denotes the order is delivered in full quantity. '0' denotes the order is not delivered in full quantity.
6: otif:    '1' denotes the order is delivered both on time and in full quantity. '0' denotes the order is either not delivered on time or not in full quantity.
