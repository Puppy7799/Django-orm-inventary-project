# Stockroom — Django Inventory

A database-driven inventory manager built with Django and SQLite. It includes a responsive product dashboard, product CRUD, category and supplier relationships, searchable/filterable/paginated inventory, stock adjustments with history, and ORM-powered inventory summaries.

## Run locally

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install -r requirements.txt
python manage.py migrate
python manage.py runserver
```

Open <http://127.0.0.1:8000/>. Add categories and suppliers in the admin at <http://127.0.0.1:8000/admin/> after creating a superuser with `python manage.py createsuperuser`.

## Included

- `Category` and `Supplier` relationships to `Product`.
- `StockMovement` audit history; stock in/out updates and movement creation run in a database transaction.
- Product create, read, update, and delete screens with server-side validation.
- Product search, category and stock-level filters, allowed-column ordering, and pagination.
- Dashboard count, unit totals, low-stock count, and inventory valuation aggregates.
- `select_related`, `prefetch_related`, database indexes, and database check constraints.

Run tests with `python manage.py test`.
