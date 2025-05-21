# fastapi-job-tracker-secured

A secure job application tracking system built with FastAPI. Users can add, edit, and filter job applications, track status, export data, and simulate real-world form security concerns like access control and data protection.

## 🎯 Learning Goals

- Handle user-authenticated form submissions
- Sanitize inputs and enforce user data separation
- Model real-world application workflows and statuses
- Export and analyze job tracking data securely

## ✅ Features

- Add, edit, delete job applications
- Fields: Company, Role, Date Applied, Status, Notes, URL
- Filter/sort by status (Applied, Interviewing, Rejected, Offer)
- User login with token-based authentication (OAuth2 or JWT)
- Optional Jinja2 dashboard frontend

## 🔐 Security Audit Points

- ❌ Are users restricted to their own data?
- ❌ Are sensitive fields (e.g. offer info) protected?
- ❌ Is input sanitized to avoid injection/XSS?
- ✅ HTTPS required in production
- ✅ Optional encryption at rest using Fernet

Full audit in [`audit-checklist.md`](./audit-checklist.md)

## 📦 Bonus Features

- Export application data to CSV
- Analytics: # of applications per week, success rate
- Email reminders for follow-ups (mock or real)
- Resume version tracking per application

## 🚀 Getting Started

```bash
git clone https://github.com/yourusername/fastapi-job-tracker-secured.git
cd fastapi-job-tracker-secured
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
uvicorn app.main:app --reload

🧪 Example API Routes
Method	Endpoint	Description
GET	/applications	View applications
POST	/applications	Create new entry
PUT	/applications/{id}	Update existing record
DELETE	/applications/{id}	Delete entry
GET	/analytics	Weekly stats (bonus feature)




