🍔 Burger King – Store Sales Dataset (2026)

Sales data from one Burger King outlet, used for an introductory Power BI masterclass.

Business question

How are the store's sales changing month by month, and which items and categories drive revenue?

Files
menu.csv (32 rows)

One row per menu item.

Column	Description
menu_item_id	Unique ID of the menu item
item_name	Name of the item (e.g. Veg Whopper)
category	Item category (Veg Burger, Chicken Burger, Meals, Sides, etc.)
price	Price of the item in ₹
order_details.csv (12,234 rows)

One row per item sold. A single order can have several rows.

Column	Description
order_details_id	Unique ID of the row
order_id	ID of the order (5,370 orders in total)
order_date	Date of the order
order_time	Time of the order
item_id	ID of the item sold (links to menu_item_id)
How the tables connect

order_details[item_id] → menu[menu_item_id] (many-to-one)

Revenue is not stored directly. Bring price in from the menu table to calculate it.

Period covered

January to March 2026.
