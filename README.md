# Vendor Management System

# Setup
1. Clone the repository:
   git clone https://github.com/your-username/vendor-management-system.git

2. Create a virtual environment:
    py -3 -m venv myenv

3. Activate the virtual environment:
    myenv\Scripts\activate

4. Install dependencies:
    pip install -r requirements.txt

5. Update database settings:
    Open vendor_manage_system/settings.py
    Update the DATABASES configuration to match your database settings

6. Running the Project
    Apply database migrations:
    python manage.py migrate

7. Create a superuser:
    python manage.py createsuperuser

8. Run the development server:
    python manage.py runserver

Access the admin panel at http://127.0.0.1:8000/admin/ and use the superuser credentials to log in.
API Endpoints

Generate Token:
    1. POST: /api/generate_token/: Generate access and refresh tokens for a vendor.
    2. POST /api/token/refresh/: Refresh the access token.

Vendor Profile:
    1. POST /api/vendors/: Create a new vendor profile.
    2. GET /api/vendors/: List all vendors.
    3. GET /api/vendors/{vendor_id}/: Retrieve a specific vendor's details.
    4. PUT /api/vendors/{vendor_id}/: Update a vendor's details.
    5. DELETE /api/vendors/{vendor_id}/: Delete a vendor.

Purchase Order:
    1. POST /api/purchase_orders/: Create a new purchase order.
    2. GET /api/purchase_orders/: List all purchase orders.
    3. GET /api/purchase_orders/{po_number}/: Retrieve a specific purchase order.
    4. PUT /api/purchase_orders/{po_number}/: Update a purchase order.
    5. DELETE /api/purchase_orders/{po_number}/: Delete a purchase order.

Acknowledge Purchase Order:
    1.POST /api/purchase_orders/{po_number}/acknowledge: Acknowledge a purchase order.

Vendor Performance Metrics:
    1. GET /api/vendors/{vendor_code}/performance: Retrieve vendor performance metrics.

Note
Ensure the virtual environment is activated whenever you work on the project.
Customize the DATABASES configuration in settings.py according to your database setup
