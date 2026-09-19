# PlaceForge — College Placement Portal (MERN Stack)
## Academic Project Report

**Project Title:** PlaceForge — College Placement Portal  
**Domain:** Full-Stack Web Development (MERN Stack)  
**Author / Student Name:** Yuvraj Singh  
**User Roles:** Student, Recruiter, Placement Coordinator (Admin)  


---

# 1. Project Title

**PlaceForge : College Placement Portal (MERN Stack)**

A centralized, role-based web application engineered to streamline campus recruitment workflows for Students, Recruiters, and the Placement Coordinator (Admin), developed using MongoDB, Express.js, React.js, and Node.js.

---

# 2. Project Objective

The primary objective of the College Placement Portal is to replace conventional, fragmented campus placement workflows—typically conducted via spreadsheets, emails, and messaging groups—with a single, centralized web application. 

Specifically, the project aims to:

1. **Centralize Placement Records:** Establish a unified database for managing job openings, student profiles, recruiter profiles, application records and their current statuses.
2. **Provide Easy Job Discovery:** Enable students to view all active campus job openings from a single directory, search for relevant openings, and view comprehensive job details.
3. **Manage Student Profiles and Resumes:** Enable students to maintain an academic and career profile (contact information, department, graduation year, skills, and academic performance) and upload their resume document.
4. **Facilitate Online Job Applications:** Allow eligible students to apply directly for job postings through the portal and easily track all submitted applications.
5. **Support Recruiter Postings and Candidate Review:** Provide corporate recruiters with tools to create company profiles, publish job postings, review applicant profiles and uploaded resumes, and update application progress.
6. **Enable Application Status Tracking:** Allow recruiters to update the status of each application and allow students to view the current status of their applications through their dashboard.
7. **Empower Placement Coordinator Oversight:** Provide the Placement Coordinator (Admin) with administrative capabilities to manage student accounts, manage recruiter accounts, oversee job postings, review all applications across the institution, and remove or deactivate inactive user accounts.
8. **Reduce Manual Placement Overhead:** Streamline coordination between students, recruiters, and the placement office, minimizing administrative errors and data fragmentation.

---

# 3. Project Description in Detail

PlaceForge is a full-stack campus placement management system built on the MERN stack. It accommodates three distinct user roles: **Student**, **Recruiter**, and **Placement Coordinator (Admin)**.

- **Student:** Registers and authenticates, maintains a personal and academic profile, uploads a resume, browses and searches for open jobs, applies for eligible positions, and monitors application status updates.
- **Recruiter:** Registers and authenticates, creates and manages a corporate profile, posts job vacancies with complete job specifications, reviews applicants and their resumes, and updates application statuses.
- **Placement Coordinator / Admin:** Logs in with administrative privileges to manage student profiles, manage recruiter accounts, oversee job listings, view all institutional applications, and deactivate inactive accounts to maintain data integrity.

### Approach:
● Designed a role-based architecture featuring dedicated dashboards tailored for Students, Recruiters, and the Placement Coordinator (Admin).  
● Implemented secure user authentication and Role-Based Access Control (RBAC) using JSON Web Tokens (JWT) to safeguard protected endpoints.  
● Designed MongoDB collections using Mongoose for Users, Students, Recruiters, Jobs, and Applications.  
● Deployed RESTful APIs supporting essential functionalities, including profile updates, job posting, job searching, online application handling, and administrative management.  
● Developed a responsive and intuitive user interface utilizing React.js and Tailwind CSS with client-side navigation via React Router.  
● Integrated document upload functionality using Multer to handle resume uploads linked to student profiles.  
● Executed end-to-end integration and functional testing across role workflows to ensure consistent data flow and system stability.

### Technologies Utilized:
● **Backend:** Node.js, Express.js, JSON Web Tokens (`jsonwebtoken`), Multer  
● **Frontend:** React.js, React Router, Axios, Tailwind CSS  
● **Database:** MongoDB, Mongoose (Object Data Modeling)  
● **Architecture:** RESTful APIs, Single-Page Application (SPA), Client-Server Architecture  

### Impact:
The platform consolidates campus recruitment into a unified portal, eliminating the confusion and delays of decentralized email threads and spreadsheets. Students gain direct access to job opportunities and can view the current status of their applications; recruiters receive a structured channel to review applicants and manage hiring stages; and the placement coordinator retains centralized governance over all campus recruitment operations.

---

# 4. Timeline Overview


| Development Phase | Planned Activities | Activities Completed (fill in from project log) |
| :--- | :--- | :--- |
| **Phase 1: Requirements & Architecture** | Analyze placement requirements, define user roles (Student, Recruiter, Admin), design MongoDB collection schemas, and initialize the project repository structure. | [Insert actual outcome] |
| **Phase 2: Authentication & Access Control** | Implement student and recruiter registration and login; integrate JWT token issuance; establish role-based access control middleware. | [Insert actual outcome] |
| **Phase 3: Student & Recruiter Profiles** | Build student profile creation and update; implement resume upload with Multer; implement recruiter company profile management. | [Insert actual outcome] |
| **Phase 4: Job Management & Discovery** | Develop recruiter job posting forms and APIs; build student job listing, keyword search, and job detail pages. | [Insert actual outcome] |
| **Phase 5: Application Workflow & Tracking** | Implement online application submission, student applied-jobs listing, recruiter applicant review, and application status update. | [Insert actual outcome] |
| **Phase 6: Administrative Oversight** | Implement admin management of student accounts, recruiter accounts, job postings, all-applications view, and inactive-user deactivation. | [Insert actual outcome] |
| **Phase 7: Frontend–Backend Integration** | Connect React components to Express REST endpoints via Axios; verify role-based navigation and end-to-end data flow. | [Insert actual outcome] |
| **Phase 8: Testing & Documentation** | Conduct functional testing across all role workflows; refine UI; compile project documentation. | [Insert actual outcome] |

---

# 5a. Key Milestones


| Milestone | Deliverable Description | Date Achieved |
| :--- | :--- | :--- |
| **Project Setup & Architecture** | Requirements analysis completed; MERN project structure and database schema established. | [Insert Date / Milestone 1] |
| **Authentication Module** | JWT registration and login operational for students and recruiters; admin authentication enabled. | [Insert Date / Milestone 2] |
| **Role-Based Access Control** | Role verification enforced on backend APIs and client-side protected routes for all three roles. | [Insert Date / Milestone 3] |
| **Profile & Resume Management** | Student academic profile and resume upload operational; recruiter company profile functional. | [Insert Date / Milestone 4] |
| **Job Posting & Search** | Recruiter job posting operational; student job directory, keyword search, and details active. | [Insert Date / Milestone 5] |
| **Application Lifecycle** | Online application submission, applied-jobs listing, recruiter applicant review, and status tracking functional. | [Insert Date / Milestone 6] |
| **Admin Control Module** | Administrative management of students, recruiters, jobs, all applications, and inactive user removal active. | [Insert Date / Milestone 7] |
| **System Integration & Testing** | End-to-end verification completed across all roles, UI polished, and project documentation compiled. | [Insert Date / Milestone 8] |

---

# 5b. Project Execution Details

### 5b.1 Role-Based Authorization
Granular permission hierarchies ensure that Students, Recruiters, and the Placement Coordinator access only role-appropriate data and functionalities. JSON Web Tokens (JWT) are verified by backend middleware on protected API endpoints, while React Router guards control page access on the client interface.

### 5b.2 User Authentication
Students and Recruiters register and log in via dedicated forms, while the Placement Coordinator accesses the platform using administrative credentials. Upon successful authentication, a signed JWT token is returned, allowing the client application to maintain an authenticated session.

### 5b.3 Student Profile & Resume Administration
Students create and maintain their academic profile, including department, graduation year, contact information, skills, and other profile information. Document upload functionality enables students to upload and store their resume file on the server, saving the file reference in their profile for recruiter evaluation.

### 5b.4 Recruiter & Job Management
Recruiters establish and maintain a company profile detailing company background, website, and contact information. Authorized recruiters create job postings specifying job title, description, location, employment type, salary, and requirements.

### 5b.5 Job Discovery & Application Pipeline
Students browse active job opportunities through a unified job listing and search for specific openings using keywords. Students submit applications online for eligible positions. The application is registered in the database, linking the student, job, and recruiter. Students can view all submitted applications in their dedicated Applied Jobs section.

### 5b.6 Applicant Review & Status Tracking
Recruiters access a dedicated list of applicants for their posted positions, review student profiles along with their uploaded resumes, and update the application status (e.g., Shortlisted, Selected, Rejected). Students can view the current status of their applications in the Applied Jobs section of their dashboard.

### 5b.7 Administrative Management Console
The Placement Coordinator oversees campus placement operations through an administrative dashboard. The administrator can review registered student accounts, manage recruiter accounts, monitor or remove job postings, view institutional application records, and deactivate or remove inactive user accounts to keep placement records current.

### 5b.8 Role-Specific Dashboards
Each authenticated user is directed to a role-tailored dashboard: Students view their profile summary, available jobs, and their applied-job statuses; Recruiters view their posted jobs and the applicants for those jobs; the Placement Coordinator reviews placement-related records and management options through the admin dashboard.

### 5b.9 Database Design

The database is implemented in MongoDB using Mongoose schemas. It comprises five core collections corresponding to the specification:

### 1. Users
- **Purpose:** Central authentication and account identity for all roles.
- **Key Fields:** `name`, `email` (unique), `password` (hashed), `role` (`student`, `recruiter`, `admin`), `isActive`, timestamps.
- **Relationships:** Links one-to-one to a `Students` profile or `Recruiters` profile. Used directly for administrative accounts.
- **Workflow Role:** Validated during login; referenced by authentication and authorization middleware.

### 2. Students
- **Purpose:** Stores student academic credentials, contact details, and resume reference.
- **Key Fields:** `user` (reference to Users), `name`, `email`, `phone`, `department`, `rollNumber`, `graduationYear`, `skills`, `cgpa`, `resume` (filename, original name, path, upload date).
- **Relationships:** Belongs to a User; referenced by Applications.
- **Workflow Role:** Maintained by the student; reviewed by recruiters upon application; managed by the admin.

### 3. Recruiters
- **Purpose:** Stores recruiter company information and contact details.
- **Key Fields:** `user` (reference to Users), `companyName`, `companyDescription`, `website`, `industry`, `location`, `contactPhone`.
- **Relationships:** Belongs to a User; referenced by Jobs and Applications.
- **Workflow Role:** Maintained by the recruiter; presented on job postings; managed by the admin.

### 4. Jobs
- **Purpose:** Represents employment opportunities published by recruiters.
- **Key Fields:** `recruiter` (reference to Users), `title`, `description`, `companyName`, `location`, `employmentType`, `workMode`, `salary`, `skills`, `applicationDeadline`, `status`.
- **Relationships:** References the posting Recruiter; referenced by Applications.
- **Workflow Role:** Created and edited by recruiters; searched and viewed by students; moderated by the admin.

### 5. Applications
- **Purpose:** Tracks student applications submitted for specific job postings.
- **Key Fields:** `student` (reference to Users), `job` (reference to Jobs), `recruiter` (reference to Users), `status` (`Applied`, `Shortlisted`, `Selected`, `Rejected`), `appliedDate`, `resume` reference.
- **Relationships:** Connects a Student, a Job, and a Recruiter.
- **Workflow Role:** Created when a student applies; reviewed and updated by recruiters; monitored by students and the admin.

### 5b.10 API Overview

The backend exposes a structured RESTful API corresponding to the required functional modules:

| Module | Method | Endpoint | Description | Permitted Roles |
| :--- | :--- | :--- | :--- | :--- |
| **Auth** | `POST` | `/api/auth/register` | Register student or recruiter account | Public |
| **Auth** | `POST` | `/api/auth/login` | Authenticate user and issue JWT token | Public |
| **Auth** | `GET` | `/api/auth/me` | Retrieve authenticated user profile | Authenticated |
| **Student** | `GET` | `/api/students/me/profile` | Retrieve own student profile | Student |
| **Student** | `POST` / `PUT` | `/api/students/me/profile` | Create or update student profile | Student |
| **Student** | `POST` | `/api/students/me/resume` | Upload or update resume document | Student |
| **Recruiter** | `GET` | `/api/recruiter/profile` | Retrieve recruiter company profile | Recruiter |
| **Recruiter** | `PUT` | `/api/recruiter/profile` | Update recruiter company profile | Recruiter |
| **Recruiter** | `POST` | `/api/recruiter/jobs` | Publish a new job posting | Recruiter |
| **Recruiter** | `GET` | `/api/recruiter/jobs` | Retrieve jobs posted by the recruiter | Recruiter |
| **Recruiter** | `GET` / `PUT` | `/api/recruiter/jobs/:id` | View or update specific job details | Recruiter |
| **Jobs** | `GET` | `/api/jobs` | List active jobs with keyword search | Student, Admin |
| **Jobs** | `GET` | `/api/jobs/:id` | View detailed job description | Student, Admin |
| **Applications** | `POST` | `/api/jobs/:jobId/apply` | Apply for an eligible job opening | Student |
| **Applications** | `GET` | `/api/student/applications` | View jobs applied for with statuses | Student |
| **Applications** | `GET` | `/api/recruiter/jobs/:jobId/applications` | View applicants for a specific job | Recruiter |
| **Applications** | `PATCH` | `/api/recruiter/applications/:id/status` | Update candidate application status | Recruiter |
| **Admin** | `GET` | `/api/admin/students` | List registered students | Admin |
| **Admin** | `PATCH` | `/api/admin/students/:id/status` | Update student status / deactivate account | Admin |
| **Admin** | `GET` | `/api/admin/recruiters` | List recruiter accounts | Admin |
| **Admin** | `PATCH` | `/api/admin/recruiters/:id/status` | Update recruiter status / deactivate account | Admin |
| **Admin** | `GET` | `/api/admin/jobs` | List all institutional job postings | Admin |
| **Admin** | `PATCH` | `/api/admin/jobs/:id/status` | Moderate or update job posting status | Admin |
| **Admin** | `GET` | `/api/admin/applications` | View all applications across the portal | Admin |

---

# 6. Snapshots / Screenshots

This section presents high-resolution snapshots captured directly from the live, running PlaceForge College Placement Portal across Student, Recruiter, and Placement Coordinator (Admin) workflows. Each snapshot illustrates the user interface, role-based interaction patterns, and data management capabilities described in the specification.

### Figure 1 — Home / Landing Page
![Figure 1 — Home / Landing Page](screenshots/fig00_landing.png)
*Public portal homepage featuring platform overview, placement statistics, key features, and role-based entry navigation.*

### Figure 2 — Student Registration Page
![Figure 2 — Student Registration Page](screenshots/fig01_student_registration.png)
*Account registration interface for students capturing academic credentials, branch, CGPA, and roll number.*

### Figure 3 — Login Page
![Figure 3 — Login Page](screenshots/fig02_login.png)
*Role-based authentication interface supporting Student, Recruiter, and Placement Coordinator logins.*

### Figure 4 — Student Dashboard
![Figure 4 — Student Dashboard](screenshots/fig03_student_dashboard.png)
*Student home interface displaying academic summary, placement readiness, quick links, and active campus drives.*

### Figure 5 — Student Profile Management
![Figure 5 — Student Profile Management](screenshots/fig04_student_profile.png)
*Profile management view for reviewing and editing academic details, graduation year, contact info, and technical skills.*

### Figure 6 — Resume Upload Interface
![Figure 6 — Resume Upload Interface](screenshots/fig05_resume_upload.png)
*Dedicated document upload panel enabling students to attach and verify their PDF resume for job applications.*

### Figure 7 — Job Listings Page
![Figure 7 — Job Listings Page](screenshots/fig06_job_listings.png)
*Directory of active campus recruitment postings displaying job title, company name, CTC, location, and eligibility criteria.*

### Figure 8 — Job Search Functionality
![Figure 8 — Job Search Functionality](screenshots/fig07_job_search.png)
*Interactive keyword search and filtering interface displaying dynamically matched campus opportunities.*

### Figure 9 — Job Details & Apply View
![Figure 9 — Job Details & Apply View](screenshots/fig08_job_details_apply.png)
*Detailed view of job description, salary breakdown, key responsibilities, and one-click application submission.*

### Figure 10 — Applied Jobs Page
![Figure 10 — Applied Jobs Page](screenshots/fig09_applied_jobs.png)
*Student application tracking console showing application history, submission dates, and real-time status badges.*

### Figure 11 — Recruiter Registration
![Figure 11 — Recruiter Registration](screenshots/fig10_recruiter_registration.png)
*Dedicated account creation interface for corporate recruiters and hiring partners.*

### Figure 12 — Recruiter Dashboard
![Figure 12 — Recruiter Dashboard](screenshots/fig11_recruiter_dashboard.png)
*Recruiter console displaying active job postings, total applications received, candidate pipeline, and quick actions.*

### Figure 13 — Company Profile Management
![Figure 13 — Company Profile Management](screenshots/fig12_company_profile.png)
*Recruiter company profile editor managing corporate details, industry domain, website, and point-of-contact info.*

### Figure 14 — Job Posting Form
![Figure 14 — Job Posting Form](screenshots/fig13_job_posting_form.png)
*Form for creating and publishing new campus recruitment drives with eligibility criteria, CTC, and role details.*

### Figure 15 — Recruiter Job Listings
![Figure 15 — Recruiter Job Listings](screenshots/fig14_recruiter_jobs.png)
*Management view of all positions published by the recruiter showing applicant counts, deadline, and posting status.*

### Figure 16 — Applicant Review Page
![Figure 16 — Applicant Review Page](screenshots/fig15_applicant_review.png)
*Applicant review interface showing candidate list, academic branch, CGPA, technical skills, and resume preview links.*

### Figure 17 — Application Status Update
![Figure 17 — Application Status Update](screenshots/fig16_status_update.png)
*Recruiter candidate evaluation modal for transitioning hiring stages (Shortlisted, Selected, Rejected) with candidate remarks.*

### Figure 18 — Admin Dashboard
![Figure 18 — Admin Dashboard](screenshots/fig17_admin_dashboard.png)
*Placement Coordinator overview console displaying institution-wide metrics, student counts, recruiter accounts, and placement stats.*

### Figure 19 — Student Management (Admin)
![Figure 19 — Student Management (Admin)](screenshots/fig18_admin_students.png)
*Administrative registry of registered students with academic performance data, placement status, and moderation controls.*

### Figure 20 — Recruiter Management (Admin)
![Figure 20 — Recruiter Management (Admin)](screenshots/fig19_admin_recruiters.png)
*Administrative interface for overseeing corporate recruiter accounts, company affiliations, and active status.*

### Figure 21 — Job Management (Admin)
![Figure 21 — Job Management (Admin)](screenshots/fig20_admin_jobs.png)
*Institutional job management console displaying all campus job postings with company links and status oversight.*

### Figure 22 — All Applications View (Admin)
![Figure 22 — All Applications View (Admin)](screenshots/fig21_admin_applications.png)
*Comprehensive portal-wide view of all student applications across companies and positions with recruitment progress tracking.*

### Figure 23 — Inactive User Management (Admin)
![Figure 23 — Inactive User Management (Admin)](screenshots/fig22_admin_inactive_user.png)
*Account moderation modal allowing the Placement Coordinator to deactivate or restore student and recruiter access.*

---

# 7. Implementation Challenges

● **Role-Based Workflow Coordination:** Designing the application around three distinct roles — Student, Recruiter, and Placement Coordinator — required maintaining separate permissions, dashboards, navigation paths, and data access rules so that each role accessed only the functionality relevant to its responsibilities.

● **Connecting the End-to-End Placement Workflow:** Integrating the full sequence of job posting → job discovery → application submission → applicant review → status update → student status tracking required consistent data handling across multiple frontend pages, backend APIs, and MongoDB collections.

● **Maintaining Consistency Across Linked Records:** The system stores users, student profiles, recruiter profiles, jobs, and applications as separate collections connected through references. Ensuring that an application correctly associated the student, job, recruiter, and resume required careful schema design and API handling.

● **Resume Upload and Profile Association:** Implementing resume upload using Multer required correctly handling multipart form requests and ensuring that the uploaded document was linked to the student's profile and made accessible during recruiter applicant review.

● **Application Status Synchronization:** When a recruiter updates an application's status, the change must be stored accurately and displayed correctly in the student's Applied Jobs view. Keeping this consistent across recruiter and student interfaces required coordinated backend and frontend handling.

● **Admin Management Without Disrupting Placement Records:** Providing the Placement Coordinator with tools to manage student accounts, recruiter accounts, job postings, and applications — including inactive-user deactivation — required handling account status carefully so that existing placement records remained intact and usable.

---

# 8. Learnings & Skills Acquired

● Full-stack application architecture and development utilizing the MERN stack (MongoDB, Express.js, React.js, Node.js).  
● Implementation of secure authentication and Role-Based Access Control (RBAC) using JSON Web Tokens (JWT).  
● RESTful API architecture, endpoint design, and asynchronous client communication using Axios.  
● Document database schema design and inter-collection references using MongoDB and Mongoose.  
● Server-side file upload handling and storage management utilizing Multer.  
● Reusable component design, responsive UI styling, and dashboard layouts using React.js and Tailwind CSS.  
● Client-side routing, URL parameter handling, and protected navigation hierarchies using React Router.  
● Practical debugging methodologies, functional integration testing, and API verification.  
● Collaborative development, version control workflows, and repository management with Git and GitHub.  
● Technical writing, requirement alignment, and structured project documentation.

---

# 9. Testimonials from Team

---

# 10. Conclusion

Manual and spreadsheet-based campus placement processes often lead to miscommunicated job notices, lost applications, and heavy administrative overhead. PlaceForge addresses these challenges by providing a centralized, MERN-based College Placement Portal.

The platform provides dedicated, role-tailored capabilities for three core user groups: Students can maintain academic profiles, upload resumes, discover jobs, apply online, and monitor their application statuses; Recruiters can maintain company profiles, publish job postings, evaluate applicants and resumes, and update recruitment progress; the Placement Coordinator (Admin) maintains complete governance over student accounts, recruiter accounts, job postings, institution-wide applications, and inactive user removal.

Developing PlaceForge provided practical, end-to-end experience across the full software lifecycle—from requirement analysis and database schema design to RESTful API implementation, JWT authentication, responsive frontend development, and system integration. The resulting portal provides a structured web-based approach to the specified placement-management requirements.

---

# 11. Acknowledgements

I would like to express my sincere gratitude to [Guide Name], [Department], [College Name], for valuable guidance, constructive feedback, and continuous support throughout the development of this project.

I am thankful to the faculty members of [Department], [College Name], affiliated to [University Name], for providing the academic direction, infrastructure, and encouragement needed to complete the College Placement Portal.

I also thank my teammates, peers, and family members for their continuous cooperation, discussions, and motivation throughout this project.
