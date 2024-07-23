This project aims to create a CRUD (Create, Read, Update, Delete) application for managing customer information using a MySQL database for storage. The backend is implemented using JSP Servlets to handle API requests, while the frontend consists of basic HTML and CSS for user interaction.

Components of the Project:
Backend (JSP Servlets):

Authentication: JWT authentication is implemented using a token-based approach. Users authenticate using their credentials, and upon successful authentication, receive a JWT token which is used to authorize subsequent API calls.
Customer Management APIs:
Create a Customer: POST request to add a new customer to the database.
Update a Customer: PUT request to modify an existing customer's information.
Get a List of Customers: GET request with pagination, sorting, and searching capabilities to retrieve a list of customers stored in the database.
Get a Single Customer: GET request to fetch details of a specific customer based on their unique ID.
Delete a Customer: DELETE request to remove a customer from the database.
Sync Customers from Remote API: Implements a functionality to fetch customer data from a remote API (https://qa.sunbasedata.com/sunbase/portal/api/assignment.jsp) and synchronize it with the local database. Existing customers in the database are updated, while new customers are inserted.
Frontend (HTML/CSS):
                   
Login Screen: Basic form for users to enter their credentials (login ID and password) to authenticate.
Customer List Screen: Displays a list of customers with options for pagination, sorting by different fields, and searching based on customer attributes.
Add New Customer Screen: Form to input details of a new customer for creation in the database.
Sync Button: Added in the second phase to trigger synchronization of customer data from the remote API.
Authentication Flow:
Users authenticate using their credentials (login_id and password) via a POST request to https://qa.sunbasedata.com/sunbase/portal/api/assignment_auth.jsp. Upon successful authentication, a JWT token is received in the response.
This token is then used as a Bearer token in the headers of subsequent API calls to authorize access.
Remote API Integration:
The project includes integration with a remote API (https://qa.sunbasedata.com/sunbase/portal/api/assignment.jsp) to fetch customer data.
A Sync button on the Customer List screen triggers a GET request to fetch the customer list from the remote API.
Retrieved customer data is compared with the local database, and existing records are updated while new records are inserted.
Use Case:
Business Use: This application can be used by businesses to manage their customer database effectively. It provides CRUD functionalities for customer management, along with synchronization capabilities with an external system (remote API).
Sync Feature: The synchronization feature ensures that the local customer database is always up-to-date with the latest data from the remote API, thereby maintaining data consistency and integrity.
Conclusion:
This project demonstrates the integration of backend CRUD operations using JSP Servlets with MySQL for data storage, along with a basic HTML/CSS frontend for user interaction. The implementation of JWT authentication ensures secure API access, while the synchronization feature enhances the application's utility by keeping customer data current and relevant.
