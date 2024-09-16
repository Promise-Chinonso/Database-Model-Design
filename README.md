### Database Model Design for FUFU Republic
_Overview:_
Fufu Republic is a popular restaurant chain in Nigeria with multiple outlets nationwide. While the core menu is standardized, some items vary by location (e.g., the Agege branch may sell Chinese Rice, while the Lekki branch might not). Customers can order online through the website or visit outlets for dine-in or take-out.

`Payment Methods:`
The restaurant accepts:

● Cash

● Debit card payments via Nomba POS terminals at outlets

● Online payments processed through gateways like Nomba Web Checkout, Paystack, Interswitch etc.

`Challenges:`

1. Inventory Management:
Variations in customer demand and menu items across branches make it challenging to maintain optimal stock levels.

3. Customer Experience:
The restaurant aims to improve the customer experience by offering personalized promotions based on purchasing behavior.

`Objective:`
Fufu Republic wants to leverage data to:

● Understand sales trends across locations, payment methods, and dining options (dine-in, take-out, online).

● Manage stock levels efficiently, reducing waste and ensuring availability.

● Enhance customer experience by analyzing purchasing habits and tailoring promotions accordingly.

__DATABASE MODEL DESIGN__

The database is modelled to have 10 tables, with attributes connecting across tables to form a relationship. There are infact 3 FACT tables which contain transactional and event data point and 7 DIMENSION tables with descriptive details providing context to the fact tables. The final look of the database is depicted in the model image below:
![FUFU_Republic_Database_Model](https://github.com/user-attachments/assets/dfe816f9-9e51-4c95-a06d-1c1f42c91d11)

__Business Process__
One typical business process Fufu republic can engage in with the help of the data it has collected in its database is efficiently monitoring customer purchase pattern and how this changes overtime. Having this insight will help the business executives maximize every chance to keep their customers satisfied and coming back for more which in turn improves the brand's repuation, revenue and awareness.

__Business Questions__
Some relevant business questions for the business process above might include:
- What items on the menu are frequently ordered?
- What items are on the order list of our top customers?
- How has the order and sales of each food item changed overtime for our top customers?
- What is the overall feedback from customers across the different branches?
- How has the rating on each food item changed in the last 3 month? etc.

  __Grain__
  The level of detail stored in the FACT tables records every transaction/sale made at the restaurant.

  __Dimensions__
  - dim_PAYMENT(Payment_Id, Payment_Channel)

