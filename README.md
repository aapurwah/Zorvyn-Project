# Zorvyn-Project


finance_tracker/
├── main.py                   ← FastAPI app + exception handlers
├── seed.py                   ← Run this for demo data
├── requirements.txt          ← pip install -r requirements.txt
├── README.md                 ← Full docs + Postman examples
└── app/
    ├── database.py           ← SQLite + SQLAlchemy setup
    ├── models.py             ← User & Transaction DB tables
    ├── schemas.py            ← Pydantic validation schemas
    ├── core/
    │   ├── security.py       ← JWT + bcrypt password hashing
    │   └── dependencies.py   ← require_admin, require_analyst guards
    ├── routes/
    │   ├── auth.py           ← register / login / me
    │   ├── users.py          ← user CRUD (admin only)
    │   ├── transactions.py   ← full CRUD + filters + pagination
    │   └── analytics.py      ← summary / categories / monthly
    └── services/
        ├── user_service.py       ← user business logic
        ├── transaction_service.py← transaction logic + filtering
        └── analytics_service.py  ← totals, breakdowns, monthly
