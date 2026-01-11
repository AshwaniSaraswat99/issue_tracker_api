# issue_tracker_api
Issue Tracker API

A backend service built using Django and Django REST Framework for managing issues, comments, labels, and reports.
This project focuses on clean API design, validation, and real-world backend concepts such as optimistic concurrency control and aggregated reporting.

🚀 Tech Stack

Python 3

Django

Django REST Framework

SQLite (default Django database)

Django ORM

📌 Implemented Features
1. Issue Management

Create, list, retrieve, and update issues

Issue status management (open, in progress, closed)

Optimistic concurrency control using a version field to prevent conflicting updates

2. Comments

Add comments to issues

Validations for non-empty comment body and author

Comments are returned along with issue details

3. Reports

Top assignees report based on the number of assigned issues

Average issue resolution time report

🧩 API Endpoints
Issues
Method	Endpoint	Description
POST	/api/issues	Create a new issue
GET	/api/issues	List all issues
GET	/api/issues/{id}	Get issue with comments
PATCH	/api/issues/{id}	Update issue (with version check)
Comments
Method	Endpoint	Description
POST	/api/issues/{id}/comments	Add a comment to an issue
Reports
Method	Endpoint	Description
GET	/api/reports/top-assignees	Get top assignees
GET	/api/reports/latency	Get average issue resolution time
⚙️ Setup Instructions
1. Clone Repository
git clone https://github.com/AshwaniSaraswat99/issue_tracker_api
cd issue_tracker_api

2. Create Virtual Environment
python -m venv .venv
source .venv/bin/activate

3. Install Dependencies
pip install -r requirements.txt

4. Run Migrations
python manage.py migrate

5. Start Development Server
python manage.py runserver

🔐 Concurrency Handling

Optimistic locking implemented using a version field on issues

Prevents overwriting changes made by concurrent updates

📈 Possible Enhancements

Bulk status updates with transactions

CSV import for bulk issue creation

PostgreSQL integration

Authentication and role-based access

Issue activity timeline

👨‍💻 Author

Ashwani Saraswat
Backend Developer | Python | Django

✅ Project Status

Core backend functionality implemented

Clean, modular codebase

Ready for review and further extension
