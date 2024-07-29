1. Login Service
	Responsibilities:
		Handle user authentication and authorization.
		Manage user login, registration, and session management.
	Interactions:
		Authenticate users for User Service.
		Provide authentication tokens for communication between services.
2. Admin Service
	Responsibilities:
		Perform adding, updating, and removing products.
		Manage product details.
	Interactions:
		Communicates with Product Service to add/update/remove products.
		Communicates with Inventory Service to update stock levels.
3. Cart Service
	Responsibilities:
		Adding, updating, and removing items in cart.
	Interactions:
		Fetch product details from Product Service.
		Interact with Inventory Service to check stock availability.
4. Inventory Service
	Responsibilities:
		Track stock levels of products.
		Adding stock, removing stock, and checking availability.
	Interactions:
		Update stock levels based on transactions processed by Order Service.
		Provide stock availability information to Product Service and Cart Service.
5. Product Service
	Responsibilities:
		Manage product catalog including creation, updating, and deletion of products.
		Provide product information like name, description, price and category.
	Interactions:
		Interact with Inventory Service to provide stock availability.
6. Order Service
	Responsibilities:
		Handle the checkout process and manage orders.
		Process payments and update order status.
		Provide order confirmations and order tracking.
	Interactions:
		Validate cart contents with Cart Service during checkout.
		Fetch product details from Product Service to ensure product data is correct.
		Update inventory levels in Inventory Service based on completed orders.
		Communicate with User Service to associate orders with user accounts.
7. User Service
	Responsibilities:
		Manage user information and profiles.
		Manage order related to users.
		Handle user registration, profile updates, and account settings.
	Interactions:
		Communicate with Login Service for authentication and user sessions.
		Provide user data to Order Service to associate orders with users.
		Manage user preferences and order history.
