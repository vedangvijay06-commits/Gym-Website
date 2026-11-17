# Project Report: Maharashtra Vyamshala Gym Website

**Student:** Vedang Vijay Panchal  
**Programme:** Bachelor of Science in Computer Science  
**Institution:** Kirti College of Arts, Science and Commerce (Autonomous), Dadar (W), Mumbai  
**Project category:** Field Project

> **Source note:** This document is a reorganized, GitHub-friendly technical overview based on the supplied 90-page project report. It preserves the report's stated technologies and design. It does not independently verify the implementation or replace the original college submission.

## 1. Introduction

The project proposes a web-based platform for gym information and management. The report identifies common issues with manual gym operations, including paper-based registration, manually maintained payment records, separate trainer records, difficulty tracking membership renewals, and the absence of a centralized database.

The proposed website aims to make gym information and selected management activities accessible through a web interface, supported by a server-side application and a cloud database.

## 2. Existing-system limitations

The report identifies these limitations in traditional manual or semi-digital gym workflows:

- Member information and payments are recorded manually.
- Searching, updating and maintaining records takes time.
- Duplicate or inconsistent records can occur.
- Renewal reminders depend on staff tracking.
- Members rely on staff for information about plans and schedules.
- Physical records and offline spreadsheets may be misplaced or damaged.
- There is no unified interface for members, trainers and administrators.

## 3. Proposed system and objectives

The proposed system is described as a client–server web application with a centralized MongoDB Atlas database.

Its stated objectives are:

1. Reduce repetitive manual work.
2. Keep member and trainer information centrally organized.
3. Provide a straightforward web interface.
4. Validate submitted information.
5. Support growth in the number of records and users.
6. Improve access to gym and membership information.

### 3.1 Features described in the report

- **Gym information:** home page, about information and facilities.
- **Membership:** membership categories, plans and registration.
- **Authentication:** login for members and administrators.
- **Member management:** adding, editing and deleting member profiles.
- **Trainer management:** trainer assignment and training-session information.
- **Payment tracking:** payment history, dues and renewal information.
- **Notifications:** alerts for renewals, dues and announcements.
- **Contact and feedback:** a way for members or visitors to submit queries.

The list above reflects the report's proposed/described scope. Verify each feature in the application before presenting it as fully implemented.

## 4. Technology stack

| Layer | Technology | Role described in the report |
|---|---|---|
| Frontend | HTML5 | Page structure and semantic content |
| Frontend | CSS3 | Layout, styling and responsive presentation |
| Frontend | JavaScript | Interactivity, form checks and dynamic updates |
| Backend | Node.js | JavaScript runtime for server-side execution |
| Backend | Express.js | Routing, middleware and HTTP request handling |
| Database | MongoDB Atlas | Cloud-hosted NoSQL data storage |
| Database integration | Mongoose | Object Data Modeling and schema validation |
| Supporting packages | cors, dotenv | Cross-origin support and environment configuration |

The report describes communication between the frontend and backend using HTTP requests and REST-style API routes.

## 5. System architecture

The report divides the system into three layers:

1. **Presentation layer:** HTML, CSS and JavaScript pages used by visitors, members and staff.
2. **Application layer:** a Node.js/Express server responsible for request handling, routing, validation and application logic.
3. **Data layer:** MongoDB Atlas, accessed through Mongoose models.

### 5.1 Request flow

```text
Visitor / Member / Admin
          |
          v
Frontend (HTML, CSS, JavaScript)
          |
       HTTP request
          |
          v
Node.js + Express server
          |
    Validation / logic
          |
          v
Mongoose models
          |
          v
MongoDB Atlas
          |
     Server response
          |
          v
Frontend displays result
```

## 6. Application modules

The project report describes these modules:

| Module | Purpose |
|---|---|
| Home | Presents gym information, facilities and benefits |
| Membership | Displays membership types and supports registration |
| Login / Authentication | Handles member and administrator sign-in |
| Database | Connects to MongoDB Atlas and stores records |
| Admin | Supports management of members, trainers and payment details |

## 7. Data and naming conventions

The report describes MongoDB Atlas as the database and Mongoose as the integration layer. It discusses collections for gym-related records such as members, trainers and payments, with references used to represent relationships.

The report's example project structure includes:

```text
gym-website/
├── index.html
├── style.css
├── script.js
├── server.js
├── setup.js
├── public/
└── models/
```

The report describes the following file roles:

- `index.html`: main entry page.
- `style.css`: visual presentation and layout.
- `script.js`: client-side interactions, validation and form submissions.
- `server.js`: Express application and routes.
- `setup.js`: MongoDB connection setup.
- `models/`: Mongoose schema/model files.
- `public/`: static assets such as images, CSS and JavaScript.

This is the structure documented in the report; check it against the actual project directory before relying on it as the current repository tree.

## 8. Validation

The report describes validation at two levels.

### 8.1 Frontend validation

- HTML form attributes such as `required`, `type`, `minlength` and `pattern`.
- JavaScript checks for empty fields and email/phone formats.
- Immediate feedback before form submission.

### 8.2 Backend validation

- Express middleware to check required request fields.
- Mongoose schema rules for required fields and data types.
- Server-side checks so that client-side validation can be bypassed without accepting invalid data.

The report gives examples involving names, email addresses, passwords, phone numbers and membership types. Actual validation rules should be confirmed in the application code.

## 9. Implementation guidance in the source report

The supplied report lists these requirements:

- Windows 10/11 or Linux
- Node.js version 14 or later
- MongoDB Atlas account
- Modern browser such as Chrome, Firefox or Edge
- Code editor such as Visual Studio Code
- Postman for API testing

It describes the following setup sequence:

1. Place the project files in a local development folder.
2. Initialize the Node.js project and install Express, Mongoose, CORS and dotenv.
3. Create a MongoDB Atlas cluster/database (the report uses the example database name `gymDB`).
4. Store the connection string in an environment variable named `DB_URI`.
5. Start the server using `node server.js`.
6. Test website forms and API routes, including validation and error responses.

**Security reminder:** Never publish a real MongoDB connection string or other secrets. Use environment variables and keep the local `.env` file out of version control.

## 10. Testing considerations

The report recommends:

- Manual browser testing of registration, login and feedback flows.
- API testing with Postman.
- Validation checks for missing or incorrectly formatted input.
- Rechecking functionality after deployment.

No independent test results are asserted in this overview.

## 11. Deployment considerations

The source report mentions cloud hosting options such as Heroku, AWS and Vercel. It also recommends protecting database access, configuring environment variables, enabling HTTPS and testing the deployed application.

The final hosting provider and deployment configuration are not specified as confirmed facts in the supplied report.

## 12. Items to confirm before final academic submission

The supplied report contains inconsistencies that should be checked rather than silently edited:

- The cover uses **“Maharashtra Vyamshala Webpage”**, while the declaration uses **“Nav Maharashtra Webpage”**; the code title includes **“Naav Maharashtra Vyamshala.”**
- The cover page states academic year **2025–2026**, while the certificate and declaration refer to **2024–2025**.
- The cover identifies **Sem III**, while the certificate identifies **S.Y.B.Sc. (Sem III)**.

Confirm the official wording and academic year with the project guide/college, then apply the same details consistently to the final submission copy.

## 13. Conclusion

The project report proposes a web-based gym website and management system using HTML, CSS and JavaScript on the frontend, Node.js and Express.js on the backend, and MongoDB Atlas with Mongoose for data storage. Its intended benefits include more organized records, easier access to membership information, input validation and reduced reliance on manual processes.

The next step for this GitHub project is to add the actual website source files and verify the documented modules against the working application.

## Source

Prepared from the user-supplied file **“nav maharashtra gym .pdf”** (90-page project report). This Markdown version is intended for repository documentation and is not a page-for-page reproduction of the original PDF.
