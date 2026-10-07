# 1. Initial Discovery

## Contents

1. [Facts](#1-facts)
2. [Assumptions](#2-assumptions)
3. [Unknowns](#3-unknowns)
4. [Stakeholders](#4-stakeholders)
5. [Goals](#5-goals)
6. [Scope](#6-scope)
    * [In Scope](#in-scope)
    * [Out of Scope](#out-of-scope)
7. [Candidate Requirements](#7-candidate-requirements)
    * [Functional Requirements](#functional-requirements)
    * [Non-Functional Requirements](#non-functional-requirements)
8. [Requirements Surgery](#8-requirements-surgery)
9.  [Reflection](#9-reflection)

*[Back to README](/README.md)*


## 1. Facts
* The college aims to implement a unified online appointment booking system for student support services, including academic counselling, financial guidance and disability support.
* Appointments are currently arranged through email, drop-ins and fragmented spreadsheets, leading to booking conflicts and lost requests.
* Students experience long response delays and have limited visibility into support staff availability.
* Support staff lack a centralised calendar view to manage daily appointments and record brief interaction notes.
* High no-show rates occur due to the absence of automated appointment reminders.


## 2. Assumptions
* Students and staff will authenticate using their existing college Sign-in credentials.
* Users will access the system primarily through web browsers on desktop and mobile devices.
* Support advisors have designated working hours, service categories and maximum daily appointment caps.
* Virtual appointments will use external video links (e.g. Zoom or MS Teams) rather than custom embedded video tools.


## 3. Unknowns
* What is the minimum cancellation notice required before a student loses or frees up an appointment slot?
* Should students be restricted to booking advisors within their own department or can they book across all campus support departments?
* How will urgent/crisis support requests be handled versus standard scheduled appointments?
* What data access boundaries apply to confidential support notes taken by advisors?


## 4. Stakeholders
* **Students:** 
  
  Need intuitive online searching, instant booking/cancellation and automated reminders.
* **Support Staff / Advisors:** 
  
  Need easy schedule management, daily appointment overviews and basic note creation tools.
* **Department Heads / Management:** 
  
  Need reports showing service demand, peak usage times and attendance rates.
* **IT Administrator:** 
  
  Needs to manage user roles and maintain the integration with the college's existing authentication system.


## 5. Goals

* Help the Support Staff keep the appointments organized.
* Help the Support Staff and Students make bookings appointments easier and quicker to manage.
* Allow authorized Students to book appointments based on their individual support needs.


## 6. Scope

### In Scope
* Student appointment searching, slot reservation, rescheduling and cancellation workflow.
* Staff appointment management and daily appointment status dashboard.
* Automated email and/or SMS notifications for booking confirmations and reminders.
* High level service usage analytics for management reporting.

### Out of Scope
* Development of custom video conferencing software.
* Deep integration with medical or formal clinical record management systems.
* Physical room/facility booking management.


## 7. Candidate Requirements

### Functional Requirements

| ID | Candidate Requirement |
|---|---|
| CR-F01 | The system should allow authenticated students to search and view available support appointment slots by service type, advisor or date. |
| CR-F02 | The system should automatically send an email confirmation and calendar invite upon successful booking. |
| CR-F03 | Support Staff should be able to set, update or block out their available consultation hours on a weekly recurring schedule. |
| CR-F04 | The system should allow authenticated students to have access to contact information for the department / a specific advisor. |

### Non-Functional Requirements

| ID | Category | Candidate Requirement |
|---|---|---|
| CR-N01 | Usability | First-time student users should be able to complete a standard appointment booking in under 2 minutes without prior training. |
| CR-N02 | Performance | Booking availability searcg results should render within 2 seconds during peak usage periods. |


## 8. Requirements Surgery

* **Vague Requirement:** 
  
    "Students should know who they are booking with."
* **Flaws:** 
  
    It is nclear what advisor details are shown, where they are displayed or how students verify qualifications.
* **Rewritten Requirement:**
  
    "The system should display the support advisor's full name, role title, department and direct contact or email on the appointment selection screen prior to booking confirmation."


## 9. Reflection

Completing initial discovery showed how important it is to turn vague user complaints into clear, measurable requirements.

Defining precise boundaries early prevents scope creep and ensures the final system actually solves the core issues.

Some requirements are difficult to understand bacause, at this stage, some of them are too vague to identify a clear solution for.

At this stage of planning, it is clear that we need to establish the main actors and speak to them in order to understand how the system could work for them.

