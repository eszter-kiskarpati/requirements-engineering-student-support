# Requirements Catalogue

## Functional Requirements

| Requirement ID | Category | Description | Stakeholder | Priority |
| :--- | :--- | :--- | :--- | :--- |
| **FR-01** | Booking | The system shall allow authenticated students to search for available consultation slots filtered by support service, advisor name or date | Students | High |
| **FR-02** | Booking | The system shall allow students to select which way they would prefer to have their session; online or in-person | Students / Support Staff | High |
| **FR-03** | Booking | The system shall allow students to submit booking requests for open consultation time slots | Students / Support Staff | High |
| **FR-04** | Conflict Mgmt | The system shall automatically flag booked appointments as unavailablly to prevent double-bookings and appointment calendar errors | Support Staff | High |
| **FR-05** | Schedule Mgmt | The system shall allow support staff/advisors to set, modify or block out their weekly appointments and availability | Support Staff | High |
| **FR-06** | Session Notes | The system shall allow authorized advisors to record private, structured interaction notes attached to a student's session history | Support Staff | Medium |
| **FR-07** | Notifications | The system shall issue immediate automated email confirmations and calendar invites to both student and advisor upon booking confirmation | Students / Support Staff | High |
| **FR-08** | Notifications | The system shall send automated appointment reminders via email 24 hours prior to the scheduled consultation time | Students | Medium |
| **FR-09** | Cancellation | The system shall allow students and staff to cancel or reschedule appointments within a configurable lead-time buffer | Students / Staff | High |
| **FR-10** | Confidentiality | The system shall restrict student session history and notes so that only authorized suppoert personnel asigned to the case might view them | It / Mgmt | High |
| **FR-11** |  | The system shall generate anonymized usage reports for department heads showing booking demand across services, peak hours and attendace rates | Department Heads | Low |
| **FR-0** | D | D | D | D |
| **FR-0** | D | D | D | D |


---


## Non-Functional Requirements

| Requirement ID | Category | Description | Target Metric | Priority |
| :--- | :--- | :--- | :--- | :--- |
| **NFR-01** | Performance | The search interface shall return available appointment slots quickly upon query submission | Display results within 2 seconds | High |
| **NFR-02** | Usability | First time student users shall be able to schedule an appointment without requiring prior system training | Complete booking in under 3 minutes | High |
| **NFR-03** | Security | System access shall require valid institutional single sign on credentials | 100% authenticated acceess via SSO/OAuth | High |
| **NFR-04** | Privacy / Security | Confidential session notes and student records shall be encrypted both in transit and at rest | Compliance with institutianal data privacy standards (GDPR)| High |
| **NFR-05** | Availability | The booking platform shall remain online and accessible during college term operating hours | 99.5% uptime during term time | Medium |
| **NFR-06** | Scalability | The system shall handle concurrent user traffic during high stress academic periods (e.g., exam weeks) | Support at least 150 simuntaneous active sessions | Medium |
| **NFR-07** | Reliability | The system shall retain audit logs for all scheduled, rescheduled and cancelled appointments | Maintain complete transaction logs for at least 1 academic year | Medium |
| **NFR-0** | D | D | D | D |