# Trisha EMS - Event Management System

Trisha EMS is a browser-based Event Management System for managing college events, competitions, student registrations, contacts, homepage highlights, reports, and role-based dashboards.

The project is built as a static HTML, CSS, and JavaScript application backed by Supabase for database, storage, and CRUD operations.

## Features

- Role-based login for Admin, Coordinator, and Student users
- Student dashboard with event and competition browsing
- Event and competition detail pages
- Student registration for competitions
- Admin dashboard for managing events, competitions, highlights, contacts, form options, and users
- Coordinator access for club-specific event and competition management
- Activity, participant, and summary report pages with PDF export support
- Supabase database schema for events, competitions, registrations, contacts, highlights, login users, and app settings

## Project Structure

```text
EMS_Project/
├── assets/
│   ├── app.js
│   ├── styles.css
│   └── Photos/
├── login.html
├── student-dashboard.html
├── admin-dashboard.html
├── events.html
├── event-details.html
├── competition-details.html
├── registration.html
├── Contact-Us.html
├── manage-events.html
├── manage-competitions.html
├── manage-homescreen.html
├── manage-contacts.html
├── manage-options.html
├── manage-users.html
├── activity-report.html
├── participants-report.html
├── summary-report.html
├── supabase-schema.sql
├── app-settings-schema.sql
└── README.md
```

## Technologies Used

- HTML5
- CSS3
- JavaScript
- Supabase JavaScript Client v2
- Supabase PostgreSQL
- html2pdf.js for report export
- Google Fonts: Outfit

## Setup Instructions

1. Open the project folder:

   ```bash
   cd EMS_Project
   ```

2. Create a Supabase project.

3. Open the Supabase SQL Editor and run:

   ```sql
   -- Run the contents of supabase-schema.sql
   ```

4. Run the app settings schema:

   ```sql
   -- Run the contents of app-settings-schema.sql
   ```

5. In Supabase Storage, create a public bucket named:

   ```text
   ems-assets
   ```

6. Check the Supabase configuration in:

   ```text
   assets/app.js
   ```

   Update `supabaseUrl`, `supabaseKey`, or the storage bucket name if you use a different Supabase project.

7. Open the application in a browser from:

   ```text
   login.html
   ```

   You can also run it through a local server such as VS Code Live Server.

## Default Login Accounts

The schema inserts demo login users:

| Role | Username | Password | Club |
| --- | --- | --- | --- |
| Admin | `admin` | `admin123` | - |
| Student | `student` | `student123` | - |
| Coordinator | `coding.coordinator` | `coding123` | Coding Club |
| Coordinator | `cultural.coordinator` | `cultural123` | Cultural Club |
| Coordinator | `sports.coordinator` | `sports123` | Sports Club |
| Coordinator | `management.coordinator` | `management123` | Management Club |

## Main Pages

- `login.html` - Login page for all roles
- `student-dashboard.html` - Student landing dashboard
- `events.html` - Event and competition catalog
- `event-details.html` - Event details
- `competition-details.html` - Competition details
- `registration.html` - Student registration form
- `Contact-Us.html` - Contact and coordinator details
- `admin-dashboard.html` - Admin dashboard
- `manage-events.html` - Create, edit, and delete events
- `manage-competitions.html` - Create, edit, and delete competitions
- `manage-homescreen.html` - Manage homepage highlights
- `manage-contacts.html` - Manage support and coordinator contacts
- `manage-options.html` - Manage dropdown/form option values
- `manage-users.html` - Manage login accounts
- `activity-report.html` - View activity registrations
- `participants-report.html` - Generate participant reports
- `summary-report.html` - Generate summary reports

## Database Tables

The Supabase schema creates these main tables:

- `events`
- `competitions`
- `registrations`
- `highlights`
- `contacts`
- `login_users`
- `app_settings`

## Notes

- This project uses simple role-based frontend session handling through browser storage.
- Passwords in the demo schema are stored as plain text for project demonstration purposes.
- For production use, replace the custom login flow with Supabase Auth and secure Row Level Security policies.
- The current schema enables broad public access policies for easy project testing.

## Author

Trisha EMS project for college event and competition management.
