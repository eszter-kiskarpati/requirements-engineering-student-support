# 3. Requirements Analysis and Specification

## Contents

1. [Information from Elicitation](#1-information-from-elicitation)
2. [Candidate Requirements](#2-candidate-requirements)
3. [Requirement Surgery](#3-requirement-surgery)
4. [Functional Requirements](#4-functional-requirements)
5. [Non-functional requirements](#5-non-functional-requirements)
6. [Business / Domain Requirements](#6-business--domain-requirements)
7. [Quality Requirements](#7-quality-requirements)
8. [Reflection](#8-reflection)


*[Back to README](/README.md)*


## 1. Information from Elicitation

### Unknowns

There is a large number of unknown factors that we heve to look at and find an answers for:

* Who can use it - We are not sure what are the constraints when it comes to the user base of the booking system
* The appointments - Unclear on multiple factors, including the services provided, rules on overbooking and cancellations, appointment types, etc.
* The Staff - No information has been provided regarding sick leaves, the scheduling and workload of the support staff
* Information and privacy - No information in regards to the guidelines of handling personal information, or on the credentials required for different functionalities
* Accessibility ans support - We do not know exactly what extra leniencies should be used for specific users and when
* Constraints - We have no information about the budgeting, no deadline for completion, or if there are any rules regarding appointment caps for individual students


## 2. Candidate Requirements
*CR-items are first drafts before refinement. This is separate from the "(Candidate)" label used in sections 4-6.*

### Functional Candidate Requirements

| ID | Candidate Requirement |
|---|---|
| CR-F01 | The system shall allow authenticated students to search and view available support appointment slots by service type, advisor or date. |
| CR-F02 | The system shall automatically send an email confirmation and calendar invite upon successful booking. |
| CR-F03 | Support Staff shall be able to set, update or block out their available consultation hours on a weekly recurring schedule. |
| CR-F04 | The system shall allow authenticated students to have access to contact information for the department / a specific advisor. |
| CR-F05 | The system shall only allow authorised users to make a booking/change appointment availability |
| CR-F06 | The system shall send automatic appointment reminders to students who booked successfuly |
---


### Non-Functional Candidate Requirements

| ID | Category | Candidate Requirement |
|---|---|---|
| CR-NF01 | Usability | First-time student users shall be able to complete a standard appointment booking in under 2 minutes without prior training. |
| CR-NF02 | Performance | Booking availability search results shall render within 2 seconds during peak usage periods. |
---


## 3. Requirement Surgery

| **Candidate ID** | **Flaw** | **Action taken** | **Resulting requirement(s)** |
| --- | --- | --- | --- |
| **CR-F01** | Compound: combines viewing available slots with filtering by three different criteria. | Split into viewing and filtering. | FR-01, FR-02 |
| **CR-F02** | Compound: combines a booking confirmation with a calendar invite. It also assumes email as the channel, which the scenario does not state. | Split in two. Channel has been removed and recorded as unknown. | FR-05, FR-06 |
| **CR-F03** | "Weekly recurring schedule" is a speculation and it does not say how exceptions such as sickness or leave are handled. | Removed the speculative detail. Kept the core which the scenario supports ("different staff may have dofferent appointment types and availability") | FR-10, FR-11 |
| **CR-F04** | Too Vague: "Have access to" and "department / a specific advisor" leaves it unclear what is shown and to who. | Narrowed to department contact details which the scenario supports ("Students currenrly contact services by email or phone") | FR-15 |
| **CR-F05** | Compound: combines two different user roles in one requirement (students booking, staff changing availability) | Split it by role so each permission can be tested seperately. | FR-16, FR-17 |
| **CR-F06** | Does not say when or by which channel the reminders should be sent | Kept the core, because the scenario asks "What reminders should be provided?". | FR-09 |
| **CR-NF01** | "Standard appointment booking" is not defined and the 2 minute target is not confirmed. | defined "Standard booking" as one appointment with one service.  | NFR-01 |
| **CR-NF02** | "Peak usage periods" is not defined and the target is not confirmed by any stakeholder. | Targe was kept at 2 seconds to match discovery and labelled as assumed. | NFR-02 |
---


## 4. Functional Requirements
*Requirements marked "(Candidate)" are not stated in the scenario and must be confirmed by stakeholders.*

| **ID** | **Requirement** | **Type** | **Priority** | **Source** | **Rationale** | **Verification** |
| --- | --- | --- | --- | --- | --- | --- |
| **FR-01** | The system shall allow an authenticated student to view available support appointment slots. | Functional | Must | Student need (CR-F01) | Students currenlty have no way of seeing availability without contacting a service. | Login as a student and confirm available slots are displayed. |
| **FR-02** <br>(Candidate) | The system shall allow a student to filter available slots by service type, advisor or date. | Functional | Should | Student need (CR-F01) | Reduces the time students spend finding a suitable slot. | Apply each filter in turns and confirm only matching slots are returned. |
| **FR-03** | The system shall display a description of each support service to help students choose the appropriate one. | Functional | Must | Student need; scenario - "students may be unsure which service they should contact" | Helps students find the right service to aid them. | Test by chechking each support service, see if a descreption is visible. |
| **FR-04** | The system shall allow an authenticated student to book an available appointment slot. | Functional | Must | Student need - Purpose of the system | Booking is the core purpose of the system. Appointments are currently arranged manually by email or phone. | Book an available slot as a student and confirm it appears as booked. |
| **FR-05** <br>(Candidate) | The system shall send the student a confirmation when a booking is made | Functional | Should | Student need (CR-F02) | Gives students a record of their bookings. | Make a test booking as a student and confirm a confirmatioin is received. |
| **FR-06** <br>(Candidate) | The system shall allow a student to add a booked appointment to their personal calendar. | Functional | Could | Student need (CR-F02) | Helps students remember  appointments. | After booking an appointment export it and makes sure it opens in a calendar application. |
| **FR-07** | The system shall allow a student to cancel a booked appointment. | Functional | Must | Student need; from scenario - "cancellatioins and changes can be difficult to manage" | Helps in lowering the amount of no-shows and frees up slots that then can be booked by other students | Test by booking an appointment then cancel it, confirm that the appointment slot is available to book again. |
| **FR-08** | The system shall allow a student to reschedule a booked appointment to another available slot. | Functional | Should | Student need; from scenario - "cancellatioins and changes can be difficult to manage" | Lets students move an appointment without cancelling, rebooking or contacting staff which reduces manual work for the staff. | Book an appointment slot, reschedule it to another available slot then confirm the new slot shown as booked and the original slot is available again. |
| **FR-09** <br>(Candidate) | The system shall send a reminder to the student before a booked appointment. | Functional | Should | Student need; from scenario - "What reminders should be provided?" (CR-F06) | Reminders may reduce missed appointments. | Make a test booking and confirm a reminder is received before the appointment time. |
| **FR-10** | The system shall allow an authorised support staff memeber to set their available appointments. | Functional | Must | Support staff need; from scenario - "different staff may have different appointment types and availability" (CR-F03) | Staff availability varies so each staff member's availability must be recorded. (Unknown if its manged by the staff or management.) | Log in as staff, set availability and confirm the new slots appear to students. |
| **FR-11** <br>(Candidate) | The system shall allow an authorised support staff member to block out times, which shall then not display to students as available. | Functional | Should | Staff need (CR-F03) | Prevents bookings at times when staff are unavailable. | Block out a time as staff and confirm it no longer appears in the student view. |
| **FR-12** <br>(Candidate) | The system shall allow a support staff member to view their upcoming appointments. | Functional | Could | Support staff need - from Discovery/stakeholder needs | Helps the staff with time management and preparation work for the day. | Login as a support staff member and check if there is a timetable available with booked appointments. |
| **FR-13** <br>(Candidate) | The system shall allow an authorised support staff member to record that a student did not attend an appointment. | Functional | Should | Support staff need; from scenario - "What happens when a student does not attend?" | The scenario asks what happens whena  student does not attend. Recording non-attendance provides data the management might need (FR-14). | Log in as staff, mark a past appointment as not attended and confirm the status is saved. |
| **FR-14** <br>(Candidate) | The system shall allow authorised management users to view reports on service demand and attendance. | Functional | Could | Management need; from Discovery/stakeholder needs | Lets the management know about important statistics regarding demand. | Create test bookings and attendance records, then log in as management and confirm the reports show matching demand and attendance figures. |
| **FR-15** <br>(Candidate) | The system shall allow a student to view contact information for each support department. | Functional | Should | Student need; from scenario - "Students currently contact services by email or phone" (CR-F04) | Lets students contact a service directly with questions that are not bookings. | Open each department's information and confirm contact details are shown. |
| **FR-16** <br>(Candidate) | The system shall only allow authenticated students to make a booking. | Functional | Must | Student need; from scenario - "Who can make an appointment?" (CR-F05) | Ensures that only legitimate users can reserve appointments. | Attempt to book an appointment using a non-student account and confirm access is blocked. |
| **FR-17** <br>(Candidate) | The system shall only allow authorised staff to change appointment availability. | Functional | Must | Staff need; from scenario - "Who can manage appointment availability?" (CR-F05) | Protects staff schedules from unauthorised changes. The roles authorised are unknown. | Attempt to change availability using a student account and confirm that access is denied. |
| **FR-18** <br>(Candidate) | The system shall no longer show a booked slot as available to other students. | Functional | Must | Discovered during activity modelling [(UC-02, Book Appointment)](/04-requirements-modelling/activity-notes.md) | Prevents double booking, which is one of the current problems named in the scenario. | Book an appointment as a student, then log in as a different student; confirm that the slot is not shown as available. |
---


## 5. Non-functional Requirements
*Requirements marked "(Candidate)" are not stated in the scenario and must be confirmed by stakeholders.*

| **ID** | **Requirement** | **Type** | **Priority** | **Source** | **Rationale** | **Verification** |
| --- | --- | --- | --- | --- | --- | --- |
| **NFR-01** <br>(Candidate) | The system shall allow first-time student users to complete a standard appointment booking in under 2 minutes without training | Non-functional (Usability) | Should | scenario - "Ease of use needs to be considered" | The ease of use is mentioned in the scenario. The 2 minute target time is an assumption. | Time a sample of first-time student users completing a standard booking. It's a pass if they complete it in under 2 minutes. |
| **NFR-02** <br>(Candidate) | The system shall display available slot search results within 2 seconds during peak usage periods. | Non-functional (Performance) | Should | CR-NF02 | Slow results could discourage use. The targeted time and peak periods need validation. | Load test the search under simulated peak demand times and measure the response time. |
| **NFR-03** | The system shall restrict access to student and appointment information to users whose role requires it. | Non-functional (Security) | Must | scenario - "Information about students and appointments must be appropriately protected." | The scenario states that student and appointment information must be appropriately protected. | Log in with each role (student / support staff / management / administrative staff (potential role, to be confirmed)) and try to view information outside that role's permissions. Confirm that access is denied. |
| **NFR-04** | The system shall meet a recognised web accessibility standard. (standard to be confirmed) | Non-functional (Accessibility) | Must | scenario - "Accessibility need to be considered." | The scenario names accessibility as a concern. The specific standard is to be confirmed with the college. | Run an accessibility audit against the supplied standard; an automated checker plus manual keyboard and screen-reader testing. |
| **NFR-05** <br>(Candidate) | The system shall be usable through current web browsers and mobile devices. | Non-functional (Compatibality) | Should | Discovery assumption: users access the system through web browsers | Discovery assumed users will access the system through web browsers on desktop and mobile. | Complete a booking on a desktop browser and on a mobile browser. Confirm all functions work and display correctly. |
--- 


## 6. Business / Domain Requirements
*Requirements marked "(Candidate)" are not stated in the scenario and must be confirmed by stakeholders.*

| **ID** | **Requirement** | **Type** | **Priority** | **Source** | **Rationale** | **Verification** |
| --- | --- | --- | --- | --- | --- | --- |
|**BR-01**| The system shall collect, store and share student and appointment iformation in line with applicable data protectioin law and college policy. | Business / Domain Requirement | Must | Data Protection Contact need (Potential stakeholder); from scenario - "information must be appropriately protected." | The college has a legal duty to protect personal data. | Review with the Data Protection Contact against the college's date protection policy. |
|**BR-02** <br>(Candidate)| The system shall make sure that when an appointment is cancelled, its slot becomes available to other students. | Business / Domain Requirement | Should | from scenario - "cancellations and changes can be difficult to manage." | When cancelled appointments stay unavailable in the system, it wastes time for the support staff. | Cancel a booked appointment and confirm the slot appears as available when viewed from a different student account. |


## 7. Quality Requirements

* **NFR-01 - Usability**

  The scenario states that ease of use needs to be considered. Since many students will only book occasionally, the system can not rely on training. NFR-01 makes "easy to use" measurable by setting a time limit for a first-time booking. The 2 minute target is an assumtion made for this project and has not been confirmed by stakeholders. It would be validated through usability testing with a sample of students and adjusted if it proves to be an unrealistic goal.

* **NFR-03 - Security**

  The scnario states that "information about students and appointments must be appropriately protected". Since the system handles personal student details and sensitive booking records, unauthorised access poses a privacy risk. NFR-03 makes "appropriately protected" enforcable by restricting data visibility based on user roles (students, management, support staff and administrative staff, a potential role still to be confirmed). The exact permission boundaries for each role are assumptions for now and will need to be confirmed with stakeholders. This requirement would be verified by logging in as each role and attempting to access records outside their permissions to cofirm that access is denied.


* **NFR-04 - Accessibility**

  The scenario names accessibility as something to consider. Students who need to use various aids need to be able to book appointments too. NFR-04 makes this actionable by requiring the system to meet a recognised web accessibility standard. Because the scenario does not specify a target level the exact standard is left open to be confirmed with the college. Once it's confirmed, it would be validated through an accessibility audit combining automated checks with manual keyboard and screen-reader testing.



## 8. Reflection


---
*[Back to top](#contents) | [Back to README](/README.md)*