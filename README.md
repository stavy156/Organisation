# Workflow Approval System

A full-stack hierarchical approval system built with Spring Boot, designed to streamline multi-level approval workflows across an organization. Models real-world organizational hierarchy — Admin, Manager, and Employee roles — with role-specific access, automated escalation, and secure endpoints.

## Overview

This project simulates a corporate approval pipeline where requests raised by Employees flow through Manager approval and, where needed, escalate to Admin oversight. The system was built with an object-oriented design at its core, encapsulating business logic within JPA entity classes and enforcing access control through interface-based abstraction.

## Features

- **Role-Based Access Control** — Three distinct roles (Admin, Manager, Employee) with tailored permissions and views, modeled as an object-oriented class hierarchy.
- **Automated Escalation** — Requests that aren't actioned within workflow rules automatically escalate up the hierarchy.
- **RESTful API** — Clean REST endpoints built with Spring Boot for handling requests, approvals, and status updates.
- **Secure Authentication & Authorization** — Endpoints secured via Spring Security, with interface-based abstraction driving role-based routing.
- **Responsive UI** — Built with vanilla JavaScript and Bootstrap for a personalized, role-based user experience.
- **Tested at Scale** — Workflows validated across 250+ test cases to ensure reliability of approval chains and escalation logic.

## Tech Stack

| Layer | Technology |
|---|---|
| Backend | Spring Boot, Spring Security, JPA |
| API | RESTful APIs |
| Frontend | HTML, CSS, JavaScript, Bootstrap |
| Database | (add your DB here, e.g. MySQL/PostgreSQL) |

## Architecture

- **Entity Layer** — JPA entity classes encapsulate business logic and map role hierarchies (Admin → Manager → Employee).
- **Access Control Layer** — Interface-based abstraction routes requests based on role, enforced via Spring Security.
- **API Layer** — REST controllers expose endpoints for request creation, approval actions, and status tracking.
- **UI Layer** — A lightweight, responsive frontend renders different views and actions depending on the logged-in user's role.

## Getting Started

### Prerequisites
- Java 17+
- Maven
- (Your database of choice, configured in `application.properties`)

### Installation
```bash
git clone <your-repo-link>
cd workflow-approval-system
mvn clean install
mvn spring-boot:run
```

The application will start on `http://localhost:8080` by default.

## Usage

1. Log in with an Admin, Manager, or Employee account.
2. Employees raise approval requests through the dashboard.
3. Managers review and approve/reject requests; unactioned requests escalate automatically.
4. Admins have full visibility and override access across the workflow.

## Future Improvements

- Email/notification integration for approval status updates
- Audit trail/history logging for compliance tracking
- Dashboard analytics for approval turnaround times

## Author

Stavya Pandey
