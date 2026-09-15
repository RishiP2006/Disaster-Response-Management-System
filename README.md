````markdown
# Disaster Response Management System

A web-based platform for managing disaster incidents and coordinating **citizens, volunteers, and emergency authorities**.

The project uses **React + Vite** for the frontend and **Supabase/PostgreSQL** for the backend and database.


## Features

- Report and manage disaster incidents
- Categorize requests by crisis type and severity
- Zone-based disaster management
- Volunteer participation in active requests
- Assign emergency authorities to incidents
- Manage emergency departments and branches
- Track request and assignment status
- Store family/group information for users

## Tech Stack

### Frontend
- React
- JavaScript
- Vite
- HTML/CSS

### Backend
- Supabase
- PostgreSQL
- Supabase JavaScript Client

### Deployment
- Vercel

## 🗄️ Database Design

The system uses a relational PostgreSQL database.

Main tables include:

- `User` – stores user information
- `request` – stores disaster requests
- `crisistype` – stores types of disasters
- `zone` – stores geographical zones
- `userhelp` – connects volunteers with requests
- `authority` – stores emergency authority information
- `authorityassignment` – connects authorities with requests
- `department` – stores emergency departments
- `deptbranch` – stores department branches
- `family` – stores family groups

### Important Relationships

```text
User ───── creates ─────> Request

User ─── UserHelp ──────> Request
        (Volunteer)

Authority ─ AuthorityAssignment ─> Request

Department ─────> Authority

Zone ─────> Users / Requests
````

## 🔄 Example Workflow

```text
Citizen reports disaster
        ↓
Crisis type and severity are selected
        ↓
Request is associated with a zone
        ↓
Relevant authorities are assigned
        ↓
Volunteers join the request
        ↓
Response status is updated
        ↓
Request is completed
```

## ⚙️ Installation

Clone the repository:

```bash
git clone https://github.com/RishiP2006/diasaster2.git
cd diasaster2
```

Install dependencies:

```bash
npm install
```

Create a `.env` file:

```env
VITE_SUPABASE_URL=your_supabase_url
VITE_SUPABASE_ANON_KEY=your_supabase_anon_key
```

Run the application:

```bash
npm run dev
```

## 🚀 Future Improvements

* Real-time emergency notifications
* Interactive disaster maps
* Live responder tracking
* Disaster analytics dashboard
* Automatic authority assignment
* Weather/disaster API integration
* Mobile application support

## Author

**Rishi**

GitHub: https://github.com/RishiP2006

```

This version is much better for a GitHub repo because it is **short enough to scan quickly**, but still highlights the **React + Supabase architecture, database design, relationships, and workflow** that an interviewer may ask you about.
```
