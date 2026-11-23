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
* The college aims to implement a unified online appointment booking system for student support services, including academic support, careers advice, learning support and more.
* Appointments are currently arranged through email and phone calls.
* The staff use informal methods for keeping track of the appointments, such as calendars and spreadsheets.
* Students are unsure as to which service they should contact that will fit their needs.
* Students do not know where and how to find available appointments.
* The staff manages appointments manually, which is unefficient and takes up a lot of their time.
* The staff availability is different across departments.
* The student and appointment information must be protected appropriately.


## 2. Assumptions
* Students and staff will authenticate using their existing college Sign-in credentials.
* Every authenticated student is able to book an appointment and see contact information for the departments.
* Users will access the system primarily through web browsers on desktop and mobile devices.
* The staff will be able to manage their own appointment calendar.
* The students will be notified about making a successful booking.
* The students will receive reminders for their upcoming appointment.
* The students will be able to change their booking date/time or to cancel it.
* The system provides available appointments after filtering for the right service.
* All services/support staff use the same system for bookings.


## 3. Unknowns
* How many student services will this appointment system include?
* How should cancellations be handled? 
* Do all the support staff manage their own schedule and opening hours?
* Do they want advisors to set their own availability manually, or should it be changed by management only?
* Should students recieve reminders about their bookings/upcoming appointments?
(* In what way should students receive reminders about their appointments?)
* Is there a department / staff member the students can contact for general information?
* Are all services able to use the same booking system?
* Should unauthorizes users be able to view information? If yes, what information?
* How will no-shows be handled/flagged?


## 4. Stakeholders & Potential Stakeholders

* **Students:** 
  
  Need intuitive online searching, instant booking/cancellation and automated reminders.
* **Support Staff / Advisors:** 
  
  Need easy schedule management, daily appointment overviews.
* **Department Heads / Management:** 
  
  Need reports showing service demand, peak usage times and attendance rates.
* **IT Administrator (Potential):** 
  
  Needs to manage user roles and maintain the integration with the college's existing authentication system.
* **Administrative Staff (Potential):**

  Needs to be able to contact departments and their support staff and have access to information about availability.
* **Data Protection Contact (Potential - discovered during elicitation):**

  Needs to make sure that student and appointment iformatioin is collected, stored and shared in line with data protetion law and college policy.


## 5. Goals

* Help the support staff keep the appointments organised.
* Help support staff and students make appointments easier and quicker to manage.
* Allow authorized students to filter through the systems based on their specific need.
* Make sure that students are reminded about their upcoming appointments to avoid frequent no-shows.
* Keep all sensitive/personal information safe and only accessable by authorized users.
* 


## 6. Scope

### In Scope
* Student appointment searching, slot reservation, rescheduling and cancellation workflow.
* Staff appointment management and daily appointment status dashboard.
* Automated email and/or SMS notifications for booking confirmations and reminders.
* Service usage analytics for management use.
* Well organized contact information section for students to use.
* 

### Out of Scope
* Development of custom video conferencing software.
* Deep integration with medical or formal clinical record management systems.
* Physical room/facility booking management.
* Implementation of a downloadable mobile app.
* Booking prioritazation based on different factors.


## 7. Candidate Requirements

### Functional Requirements

| ID | Candidate Requirement |
|---|---|
| CR-F01 | The system shall allow authenticated students to search and view available support appointment slots by service type, advisor or date.|
| CR-F02 | The system shall automatically send an email confirmation and calendar invite upon successful booking |
| CR-F03 | Support Staff shall be able to set, update or block out their available consultation hours on a weekly recurring schedule |
| CR-F04 | The system shall allow authenticated students to have access to contact information for the department / a specific advisor |
| CR-F05 | The system shall only allow authorised users to make a booking/change appointment availability |
| CR-F06 | The system shall send automatic appointment reminders to students who booked successfuly |
 
### Non-Functional Requirements

| ID | Category | Candidate Requirement |
|---|---|---|
| CR-N01 | Usability | First-time student users shall be able to complete a standard appointment booking in under 2 minutes without prior training. |
| CR-N02 | Performance | Booking availability searcg results shall render within 2 seconds during peak usage periods. |


## 8. Requirements Surgery

* **Vague Requirement:** 
  
    "Students should know who they are booking with."
* **Flaws:** 
  
    It is unclear what advisor details are shown, where they are displayed or how students verify qualifications.
* **Rewritten Requirement:**
  
    "The system should display the support advisor's full name, role title, department and direct contact or email on the appointment selection screen prior to booking confirmation."


## 9. Reflection

Completing initial discovery showed how important it is to turn vague user complaints into clear, measurable requirements.

Defining precise boundaries early prevents scope creep and ensures the final system actually solves the core issues.

Some requirements are difficult to understand bacause, at this stage, some of them are too vague to identify a clear solution for.

At this stage of planning, it is clear that we need to establish the main actors and speak to them in order to understand how the system could work for them.

