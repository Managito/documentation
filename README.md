# 📄 Software Requirements Specification (SRS)

## Project Name: Managito

---

## 1. Introduction

### 1.1 Purpose

This document defines the requirements for the **Managito** project management application. The goal is to provide a simple yet professional project management experience for:

- Individual developers
- Freelancers
- Small, amateur teams

**The application should provide:**

- Task management
- Note-taking and organization
- File management
- Documentation
- Mind mapping
- Reporting
- AI-assisted guidance
- Calendar and reminders
- Simple collaboration for small teams (expandable in the future)

---

### 1.2 Scope

Managito will:

- Work on both web and mobile platforms (cross-platform)
- Target individual users and small teams (max. 5-10 people)
- Avoid the complexity of large enterprise solutions while offering:
  - Project creation and management
  - Task, note, file, and calendar management
  - Simple collaboration and sharing
- Increase productivity through AI integrations

---

### 1.3 Definitions, Acronyms, Abbreviations

- **AI** – Artificial Intelligence
- **CRUD** – Create, Read, Update, Delete
- **SRS** – Software Requirements Specification
- **UI** – User Interface
- **UX** – User Experience
- **JWT** – JSON Web Token

---

### 1.4 References

- IEEE 830 – Software Requirements Specification Standard
- RESTful API Design Principles
- OWASP Security Guidelines
- Material Design Guidelines

---

## 2. Overall Description

### 2.1 Product Perspective

Managito:

- Is a brand-new product
- Uses its own backend and frontend infrastructure
- Integrates with AI services (e.g., OpenAI, DeepSeek, Claude, etc.)
- Offers a free plan for small teams
- May introduce premium features for larger teams

---

### 2.2 Product Functions (Overview)

- **Project Management:** Create, edit, delete, archive projects
- **Task Management:** Create tasks, update, add sub-tasks, label
- **Note Management:** Create, edit, summarize, label notes
- **File Management:** Upload, share, version control
- **Documentation:** Create, update, delete documentations in markdown or HTML format (or any other)
- **Mind Mapping:** Create mind maps, add nodes, draw connections
- **AI Assistant:** Suggest tasks, generate reports, perform risk analysis, AI Chat (like ChatGPT or others)
- **Reporting:** Track project progress, task statistics, time reports
- **Reminder:** Create, update, delete reminders
- **Calendar:** Display tasks and reminders
- **Notifications:** Push, email, sms, in-app
- **Multi-language support:** Localization support (Englist, Turkish, German)
- **User authentication:** JWT-based login

---

### 2.3 User Classes and Characteristics

| User Type             | Characteristics                                      |
|------------------------|------------------------------------------------------|
| Individual Developer   | Works solo, prefers simple usage. Often manages multiple small projects alone and needs fast navigation, AI assistance for generating tasks, and integrated note-taking. Values speed and simplicity. |
| Small Team Member      | Works collaboratively on projects with others. Responsible for individual tasks but participates in shared resources such as notes, files, and project discussions. Needs clear task assignments, notifications, and easy communication. |
| Project Manager        | Oversees entire projects, tracks progress, manages team workloads, and generates reports. Requires dashboards, analytics, risk reports, Gantt charts, and ability to assign or reassign tasks. Often uses calendar views and reminders to stay organized. |
| System Administrator   | Configures system-wide settings, manages user accounts and permissions, and handles billing or premium features. Focuses on security, scalability, backups, and overall system health. Usually accesses logs, analytics, and user management tools. |

---

#### Detailed Descriptions

#### Individual Developer

- **Responsibilities:**
  - Creates projects and manages them solo
  - Adds tasks, tracks personal progress
  - Writes personal notes and mind maps
  - Uses AI assistant to simplify tasks or generate summaries
- **Needs:**
  - Quick navigation
  - Minimal UI complexity
  - Ability to work offline on mobile
  - Time tracking for freelance billing
- **Primary Scenarios:**
  - Starts a project from scratch
  - Uses mind map to organize ideas
  - Quickly captures notes while coding

---

#### Small Team Member

- **Responsibilities:**
  - Completes tasks assigned by others
  - Collaborates in shared documents and discussions
  - Uploads or accesses shared files
- **Needs:**
  - Clear task assignments
  - Easy notification system
  - In-app chat for quick communication
  - Ability to comment on tasks or notes
- **Primary Scenarios:**
  - Checks today’s tasks
  - Uploads a document for team review
  - Adds comments to shared notes

---

#### Project Manager

- **Responsibilities:**
  - Oversees multiple projects simultaneously
  - Monitors task progress and deadlines
  - Manages workload distribution across team
  - Generates progress and risk reports
- **Needs:**
  - High-level dashboards
  - Graphs and charts for visual reporting
  - Gantt charts for scheduling
  - AI-driven risk analysis and recommendations
- **Primary Scenarios:**
  - Reviews project health
  - Adjusts task deadlines
  - Exports reports for clients or stakeholders

---

#### System Administrator

- **Responsibilities:**
  - Manages overall system settings
  - Oversees user management and permissions
  - Ensures security compliance and backups
  - Configures integrations and API keys
- **Needs:**
  - Strong security controls
  - Role-based access management
  - Audit logs and monitoring tools
  - Scalability settings for larger user bases
- **Primary Scenarios:**
  - Adds or removes users
  - Configures single sign-on
  - Reviews system performance metrics

---

### 2.4 Operating Environment

- Web → Modern browsers (Chrome, Edge, Safari, Firefox)
- Mobile → Android, iOS
- Backend → .NET Core
- API → RESTful
- Database → PostgreSQL
- Cloud Storage → Firebase Storage or AWS S3
- Deployment → AWS, Azure or Google Cloud Platform

---

### 2.5 Constraints

- Must be GDPR compliant
- All text must support UTF-8
- Fully responsive design
- Mobile web minimum width: 360px
- Free plan limited by API usage quotas

---

### 2.6 Assumptions and Dependencies

- Users have internet access
- AI services (OpenAI, DeepSeek) may be free or usage-limited
- Domain name is available
- Development team consists of at least 2-3 people

---

## 3. Functional Requirements

All **functional requirements** below define the core capabilities of the project management system.

---

### FR-1 Project Management

- FR-1.1 → Users shall be able to create projects
- FR-1.2 → Users shall assign names, descriptions, and colors to projects
- FR-1.3 → Users shall change project statuses
- FR-1.4 → Users shall delete projects
- FR-1.5 → Users shall archive projects
- FR-1.6 → Users shall search for projects

---

### FR-2 Task Management

- FR-2.1 → Users shall create tasks
- FR-2.2 → Users shall add task titles, descriptions, tags, and due dates
- FR-2.3 → Users shall add sub-tasks
- FR-2.4 → Users shall change task statuses
- FR-2.5 → Users shall sort tasks
- FR-2.6 → Users shall add comments to tasks
- FR-2.7 → Users shall search tasks
- FR-2.8 → Users shall track task completion percentages
- FR-2.9 → Users shall get AI assistance to expand task details

---

### FR-3 Note Management

- FR-3.1 → Users shall create notes
- FR-3.2 → Users shall add titles, content, and tags to notes
- FR-3.3 → Users shall attach files and images
- FR-3.4 → Users shall summarize notes using AI
- FR-3.5 → Users shall convert notes into tasks
- FR-3.6 → Users shall share notes
- FR-3.7 → Users shall search notes

---

### FR-4 File Management

- FR-4.1 → Users shall upload files
- FR-4.2 → Users shall delete files
- FR-4.3 → Users shall share files
- FR-4.4 → Users shall preview files
- FR-4.5 → Users shall have file versioning

---

### FR-5 Mind Mapping

- FR-5.1 → Users shall create new mind maps
- FR-5.2 → Users shall add nodes
- FR-5.3 → Users shall draw links between nodes
- FR-5.4 → Users shall export mind maps
- FR-5.5 → Users shall generate mind maps with AI suggestions

---

### FR-6 Reporting

- FR-6.1 → Users shall generate task statistics reports
- FR-6.2 → Users shall view project progress reports
- FR-6.3 → Users shall export reports to PDF/Excel
- FR-6.4 → Users shall generate AI-based risk analysis reports

---

### FR-7 Calendar and Reminders

- FR-7.1 → Users shall view tasks in a calendar
- FR-7.2 → Users shall set reminders
- FR-7.3 → Users shall integrate external calendars

---

### FR-8 Notifications

- FR-8.1 → Users shall receive push notifications
- FR-8.2 → Users shall receive email notifications
- FR-8.3 → Users shall customize notification settings (enable/disable)

---

### FR-9 User Management

- FR-9.1 → Users shall register new accounts
- FR-9.2 → Users shall log in
- FR-9.3 → Users shall reset passwords
- FR-9.4 → Users shall update profile information
- FR-9.5 → Users shall delete accounts

---

### FR-10 AI Assistant

- FR-10.1 → Users shall receive task suggestions
- FR-10.2 → Users shall get time estimates for tasks
- FR-10.3 → Users shall summarize notes
- FR-10.4 → Users shall generate risk analysis reports
- FR-10.5 → Users shall receive mind map suggestions

---

## 4. Non-Functional Requirements (NFR)

---

### NFR-1 Performance

- NFR-1.1 → Web app must load within 2 seconds
- NFR-1.2 → Mobile app must launch within 3 seconds
- NFR-1.3 → API responses should be under 500ms

---

### NFR-2 Security

- NFR-2.1 → Must use JWT authentication
- NFR-2.2 → Must enforce HTTPS
- NFR-2.3 → Passwords must be stored as hashes
- NFR-2.4 → Private files must be inaccessible to public
- NFR-2.5 → Must implement OWASP Top 10 best practices

---

### NFR-3 Usability

- NFR-3.1 → UI/UX must be user-friendly
- NFR-3.2 → Must be fully responsive
- NFR-3.3 → Should support light/dark themes
- NFR-3.4 → Must support multiple languages

---

### NFR-4 Reliability

- NFR-4.1 → System must have backups in case of server failures
- NFR-4.2 → Data must be backed up daily to prevent data loss

---

### NFR-5 Compatibility

- NFR-5.1 → Must work on all modern browsers
- NFR-5.2 → Must be compatible with Android and iOS
- NFR-5.3 → Must support export of documents in PDF and Excel formats

---

### NFR-6 Scalability

- NFR-6.1 → Must support at least 10,000 users
- NFR-6.2 → Should be prepared for premium plans for larger teams

---

### NFR-7 Maintainability

- NFR-7.1 → Code must be modular and maintainable
- NFR-7.2 → Must use a version control system (e.g., Git)

---

### NFR-8 Error Handling

- NFR-8.1 → Error messages must be user-friendly
- NFR-8.2 → System must have proper logging
- NFR-8.3 → Critical errors must be reported (e.g., via Sentry)

---

### NFR-9 Accessibility

- NFR-9.1 → Must comply with WCAG 2.1 accessibility standards
- NFR-9.2 → Must support keyboard navigation

---

## 5. External Interfaces

---

### 5.1 User Interfaces

- Web UI
- Mobile UI
- Fully responsive design
- Simple, modern, minimalist interface

---

### 5.2 Hardware Interfaces

- On mobile devices:
    - Camera access (for uploading photos)
    - Push notifications

---

### 5.3 Software Interfaces

- OpenAI API
- DeepSeek API
- Firebase Auth
- Firebase Storage
- Stripe API (for premium plans)
- Google Calendar API

---

### 5.4 Communication Interfaces

- RESTful API
- WebSocket (for chat features)
- HTTPS

---
