# Problem Statement, stakeholders and Goals

## Contents

- [Facts](#facts)
- [Assumptions](#assumptions)
- [Unknowns](#unknowns)
- [Stakeholders and Goals](#stakeholders-and-goals)
- [Scope Boundaries](#scope-boundaries)
    - [In Scope](#in-scope)
    - [Out of Scope](#out-of-scope)
- [Out of Scope](#out-of-scope)
- [Candidate Requirements](#candidate-requirements)
    - [Functional Requirements](#functional-requirements)
    - [Non-Functonal Requirements](#non-functional-requirements)
- [Requirements Surgery](#requirements-surgery)
- [Reflection](#reflection)

## Facts
* The college aims to implement a unified online appointment booking system for student support services (academic counselling, financial guidance and disability support).
* Appointments are currently arranged through emails, drop-ins and fragmanted spreadsheets, leading to booking conflicts and lost requests.
* Students experience long response delays and lack of clear visibility into support staff availability.
* Support staff lack a centralized calendar view to manage daily appointments and record brief interaction notes.
* High no-show rates occur due to the absence of automated appointment reminders.

## Assumptions
* Students and staff will authenticate using their existing college Sign-in credentials.
* Users will access the system primarily via web browsers on desktop and mobile devices.
* Support advisors have designated working hours, service categories and maximum daily appointment caps.
* Virtual appointments will utilize external video links (e.g. Zoom or MS Teams) rather than custom embedded video tools.

## Unknowns
* What is the minimum cancellation notice required before a student loses or frees up an appointment slot?
* Should students be restricted to booking advisors within their own department or can they book across all campus support departments?
* How will urgent/crisis support requests be handled versus standard scheduled appointments?
* What data access boundaries apply to confidential support notes taken by advisors?

## Stakeholders and Goals
* **Students:** Need intuitive online searching, instant booking/cancellation and automated reminders.
* **Support Staff / Advisors:** Need easy schedule management, daily appointment overviews and basic note logging tools.
* **Department Heads / Management:** Need aggragate reporting on service demand, peak usage hours and attendance rates.
* **IT Administrator:** Requires streamlined user role management and integration with the use of the existing college authentication systems. 

## Scope Boundaries
### In Scope
* Student appointment searching, slot reservation, rescheduling and cancellation workflow.
* Staff automated mamagement and daily appointment status dashboard.
* Automated email and/or SMS notifications for booking confirmations and reminders.
* High level service usage analytics for management reporting.

### Out of Scope
* Development of custom video conferencing software.
* Deep integration with medical or formal clinical record management systems.
* Physical room/facility booking management.

## Candidate Requirements
### Functional Requirements
* The system should allow authenticated students to search and view available support appointment slots by service type, advisor or date.
* The system should automatically send an email confirmation and dynamic calendar invite upon successful booking.
* Support staff should be able to set, update or block out their available consultation hours on a weekly recurring schedule.
### Non-Functional Requirements
* **Usability:** First time student users should be able to complete a standard appointment booking in under 2 minutes without prior training.
* **Performance:** Booking availability search results should render within 2 seconds during peak usage periods.

## Requirements Surgery
* **Vague Requirement:** "Students should know who they are booking with."
* **Flaws:** Unclear what advisor details are shown, where they are displayed or how students verify qualifications.
* **Rewritten Requirement:** "The system should display the support advisor's full name, role title, department and direct contact or email on the appointment selection screen prior to booking confirmation."

## Reflection
Completing this initial discovery phase highlights the necessity of transforming broad operational frustrations, such as missed appointments and scheduling conflicts into structured, measurable requirements.

Establishing clear scope boundaries early prevents feature sprawl and keeps the development focus on the core booking experience.