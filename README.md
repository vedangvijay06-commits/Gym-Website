# Maharashtra Vyamshala Gym Website

A college field-project documenting a web-based gym website and management system for **Naav Maharashtra Vyamshala**.

The project report describes a responsive frontend built with HTML, CSS and JavaScript, a Node.js/Express backend, and MongoDB Atlas for data storage.

## Project at a glance

| Area | Technology / approach |
|---|---|
| Frontend | HTML5, CSS3, vanilla JavaScript |
| Backend | Node.js, Express.js |
| Database | MongoDB Atlas |
| Database integration | Mongoose |
| Supporting packages mentioned in the report | cors, dotenv |
| API style | HTTP / REST-style endpoints |

## Intended capabilities

The project report describes the following system areas:

- Gym information and home page
- Membership plans and registration
- Member login and authentication
- Member and trainer management
- Payment and renewal tracking
- Contact and feedback
- Client-side and server-side input validation

These are capabilities described in the submitted project report; the presence and completeness of each feature should be verified against the actual application source code.

## Documentation

- [Project overview and technical documentation](docs/PROJECT-REPORT.md)

The original 90-page college report was used as the source for this documentation. The report includes system analysis, proposed design, technology stack, database discussion, naming conventions, program descriptions, validation, implementation guidance, code excerpts and screen layouts.

## Development setup (as described in the report)

### Prerequisites

- Node.js (the report specifies version 14 or later)
- MongoDB Atlas account and a database
- A code editor such as Visual Studio Code
- A modern web browser

### Install dependencies

From the project directory:

```bash
npm init -y
npm install express mongoose cors dotenv
```

### Configure environment variables

Create a `.env` file and set your MongoDB connection string:

```env
DB_URI=your_mongodb_atlas_connection_string
PORT=3000
```

Do not commit real credentials, database connection strings, API keys or passwords. Keep `.env` private and add it to `.gitignore`.

### Start the server

The report describes starting the application with:

```bash
node server.js
```

The exact commands and file paths should be checked against the current application source before running them. This repository currently contains project documentation; the website's source-code files have not yet been added.

## Repository structure

```text
Gym-Website/
├── README.md
└── docs/
    └── PROJECT-REPORT.md
```

## Academic project details

- **Student:** Vedang Vijay Panchal
- **Programme:** Bachelor of Science in Computer Science
- **Institution:** Kirti College of Arts, Science and Commerce (Autonomous), Dadar (W), Mumbai
- **Project:** Maharashtra Vyamshala Webpage

## Report consistency note

The supplied report uses more than one project-name form (including “Maharashtra Vyamshala Webpage” and “Nav Maharashtra Webpage”) and contains different academic-year references on its cover and certificate/declaration pages. These details have deliberately not been silently changed. Confirm the official project title and academic year with the college before using the report as a final submission copy.

## Future improvements

- Add the actual frontend and backend source files.
- Add approved screenshots of the running website.
- Verify each documented feature against the implementation.
- Add setup instructions based on the final source tree.
- Add tests and deployment instructions when available.

---

*Prepared from the supplied college project report. This README documents the project as described in that source; it is not a claim that the application has been independently tested or deployed.*
