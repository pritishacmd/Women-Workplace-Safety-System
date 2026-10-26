# Women Workplace Safety and Incident Resolution Management System

## Overview

The Women Workplace Safety and Incident Resolution Management System is a web-based application designed to support workplace safety through structured incident reporting, investigation, and resolution tracking. It provides a centralized platform for reporting workplace incidents and managing them through a defined resolution process.

The system supports three user roles: Users, Committee Members, and Administrators. Each role has specific responsibilities for reporting, investigating, and managing incidents.

## Objectives

- Provide a centralized platform for workplace incident reporting.
- Support anonymous incident submissions.
- Enable committee members to review and investigate reported incidents.
- Track incidents from submission to final resolution.
- Provide role-based access for users, committee members, and administrators.
- Maintain organized incident records using a relational database.

## Key Features

- **Incident Reporting:** Submit workplace safety incidents through a web interface.
- **Anonymous Reporting:** Support anonymous incident submissions.
- **Role-Based Access:** Separate functionality for users, committee members, and administrators.
- **Incident Tracking:** Monitor the progress of reported incidents.
- **Investigation Management:** Support the review and investigation of submitted reports.
- **Resolution Workflow:** Track incidents through the following statuses:
  - `REPORTED`
  - `UNDER_INVESTIGATION`
  - `ACTION_TAKEN`
  - `CLOSED`
- **Database Management:** Store and manage incident records using Oracle Database.

## Technology Stack

| Component | Technology |
|---|---|
| Frontend | HTML, CSS, JavaScript |
| Backend | Node.js, Express.js |
| Database | Oracle Database XE 11g |
| Database Client | Oracle SQL Developer |
| API Communication | REST APIs |

## System Architecture

The application follows a client-server architecture.

1. **Frontend:** Provides the interface for submitting incidents and viewing relevant information.
2. **Backend:** Processes application requests, applies business logic, and handles communication with the database.
3. **Database:** Stores incident reports, user information, and related records in Oracle Database.

## Incident Resolution Workflow

```text
Incident Report Submitted
          |
          v
       REPORTED
          |
          v
UNDER_INVESTIGATION
          |
          v
     ACTION_TAKEN
          |
          v
        CLOSED
```

## User Roles

### 1. User
- Submit workplace incident reports.
- Access permitted incident-related information.
- Track reports where authorized.

### 2. Committee Member
- Review submitted reports.
- Investigate incidents.
- Update investigation and resolution status.

### 3. Administrator
- Manage authorized system operations.
- Oversee user access and incident records according to assigned permissions.

## Project Structure

The project can be organized into the following components. Actual filenames may differ depending on the implementation.

```text
women-workplace-safety-system/
├── frontend/
├── backend/
├── database/
└── README.md
```

## Setup and Installation

### Prerequisites

- Node.js and npm
- Oracle Database XE 11g
- Oracle SQL Developer
- Git

### 1. Clone the Repository

```bash
git clone https://github.com/pritishacmd/women-workplace-safety-system.git
cd women-workplace-safety-system
```

### 2. Configure the Database

1. Start Oracle Database.
2. Open Oracle SQL Developer.
3. Connect to your configured Oracle database.
4. Execute the project's database scripts in the required order.
5. Configure the backend database connection using your local credentials.

### 3. Install Backend Dependencies

Navigate to the backend directory:

```bash
cd backend
npm install
```

If the backend uses environment variables, create a local `.env` file and configure the values required by the application.

Never commit `.env` files, database passwords, or other secrets to GitHub.

### 4. Start the Backend

Run the start command defined in `backend/package.json`. For example:

```bash
npm start
```

If the project uses a different script, run the appropriate command.

### 5. Run the Frontend

Open the frontend entry point or use the development server configured for the project.

Ensure that the frontend API configuration points to the running backend.

## Security Considerations

- Protect database credentials and environment variables.
- Enforce role-based authorization on protected backend routes.
- Validate incoming user input.
- Restrict access to confidential incident information.
- Protect reporter identities and sensitive incident details.
- Use secure authentication and token handling where implemented.

## Future Enhancements

- Email notifications for incident status updates.
- Incident analytics and reporting dashboards.
- Audit logs for investigation and resolution activities.
- Improved accessibility and mobile responsiveness.
- Enhanced privacy controls and configurable reporting policies.

## Learning Outcomes

This project provides practical experience in:

- Relational database design and SQL.
- Full-stack web application development.
- REST API development and integration.
- Role-based access management.
- Incident lifecycle and workflow management.
- Application security and data privacy considerations.

## Author

**GitHub:** [pritishacmd](https://github.com/pritishacmd)

## License

This project was developed for academic purposes. A formal license can be added if the project is intended for public reuse or distribution.
