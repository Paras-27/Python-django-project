
Invoice Django REST API
This Django application implements a RESTful API for managing invoices and their associated details. The main URL for accessing invoices is /invoices/, with additional endpoints for specific invoice details.

API Endpoints
1. List and Create Invoices
URL: /invoices/
HTTP Methods: GET, POST
Description: Get a list of all invoices or create a new invoice.

2. Retrieve, Update, and Delete Single Invoice
URL: /invoices/<int:pk>/
HTTP Methods: GET, PUT, DELETE
Description: Retrieve, update, or delete a specific invoice by providing its primary key (<int:pk>).
Models
1. Invoice Model
Fields:
date (DateField): Invoice date.
customer_name (CharField): Name of the customer.
2. InvoiceDetail Model
Fields:
invoice (ForeignKey): Reference to the associated invoice.
description (CharField): Description of the invoice detail.
quantity (IntegerField): Quantity of items.
unit_price (DecimalField): Unit price of the item.
price (DecimalField): Total price for the quantity.
Running Tests
Ensure the correctness of API endpoints by running test cases. Execute the following command:

python manage.py test
Dependencies
Django
Django Rest Framework
Setup Instructions


python manage.py migrate
Run the development server:

python manage.py runserver
Now, you can access the API at http://127.0.0.1:8000/invoices/ and test the provided functionalities.

