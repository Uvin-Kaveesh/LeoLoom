# LeoLoom

**A project management and reporting portal for a volunteer service club**

LeoLoom is a digital secretary workspace developed during the 2026/27 service year. It brings project planning, responsibility assignments, progress tracking, evidence, and reporting information into one shared system. This repository is a public project report. The operational source repositories and club records remain private.

## The problem

Project details were spread across personal devices, messages, documents, and spreadsheets. Preparing a report meant collecting updates again from different people. A change of officers could also leave the next team without a searchable account of earlier work. LeoLoom was built to make each project a durable, structured record that can be updated throughout its lifecycle.

## Development path

1. An earlier single-file browser page stored information locally on one device.
2. The first shared implementation introduced a Java Spring Boot backend, SQLite persistence, a project dashboard, committee records, project photos, and spreadsheet-compatible export. Its administrator model used a shared password.
3. The later portal expanded the system with individual accounts, Administrator/Admin/Member roles, email verification, member profiles, activity records, controlled deletion requests, additional project media, and a Progressive Web App interface. The final repository also contains a TypeScript serverless API for hosted operation.

The second implementation is the final contribution. The earlier repository represents a development stage of the same project.

## What the portal supports

| Area | Capability |
| --- | --- |
| Project records | Planning details, dates, venue, status, subtasks, responsibilities, and notes |
| Reporting | Participation, beneficiaries, service hours, finances, community needs, and spreadsheet-compatible export |
| Tracking | Search, status filters, record-completeness progress, and due-date indicators |
| People | Committee records, member profiles, and links between accounts and project roles |
| Media | Project thumbnails, covers, and organized photographs |
| Administration | Role-based access, shared categories, activity history, and deletion review |

Progress represents the completeness of a project record. It is separate from the project's operational status, so a completed activity can still show missing reporting information. Historical assignments remain on project records when committee membership changes.

## Technical outline

- **Backend:** Java 17, Spring Boot, REST endpoints, and Spring Data JPA.
- **Data:** SQLite for local use; the final implementation includes PostgreSQL support for hosted deployments.
- **Hosted API:** A TypeScript serverless API is present alongside the Spring Boot application.
- **Frontend:** HTML, CSS, and framework-free JavaScript, with responsive layouts and Progressive Web App files.
- **Media:** Images are reduced before upload and stored separately from ordinary project records. The final implementation includes private object-storage support.
- **Access:** Individual accounts with Administrator, Admin, and Member roles. Public member information is separated from private contact details.

These are implementation capabilities visible in the private source. This report does not claim measured reductions in reporting time, adoption figures, or production uptime.

## Contribution and outcome

LeoLoom turns secretary work into an ongoing workflow: create a project record early, assign people, add evidence and impact details as work proceeds, then use the same record for reporting and handover. The resulting archive gives future officers a clearer account of what was planned, who was responsible, and what was delivered.

The key design choices were to preserve historical project assignments, separate status from documentation completeness, restrict destructive operations, keep normal project views lightweight, and expose only suitable member details through public-facing responses.

## Privacy and publication

This public report intentionally omits the club's identity, member names, private project records, credentials, internal endpoints, and operational URLs. It is a description of the work, not a deployment guide or a release of the private application source.

## Scope of this report

This summary was prepared from the two private development repositories and the LeoLoom project report. It describes the evolution and documented capabilities of the system. It does not include source code, screenshots, or data from those private materials.

