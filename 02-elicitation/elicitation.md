# 2. Elicitation


## Contents

1. [Stakeholders' Needs and Concerns](#1-stakeholders-needs-and-concerns)
2. [Unknowns](#2-unknowns)
3. [Information Sources](#3-information-sources)
4. [Elicitation Questions](#4-elicitation-questions)
5. [Candidate Requirement](#5-candidate-requirement)


*[Back to README](/README.md)*


## 1. Stakeholders' Needs and Concerns

*Administrative Staff* and the *IT Administrator* were identified as potential stakeholders during discovery.

* **Students**
    * *Needs:* - Intuitive online searching, instant booking / cancellation, clear contact details and automated appointment reminders.
    * *Concerns:* - Unceartainty over which support service to contact, difficulty finding available appointment slots and missing scheduled appointments caused by lack of reminders.
* **Support Staff / Advisors**
    * *Needs:* - Easy schedule management, daily appointment overviews, autmated schedule updates (cancellations / bookings).
    * *Concerns:* - Spending excessive time managing appointments manually, dealing with unmanaged no-shows and handling last minute cancellations.
* **Department Heads / Management**
    * *Needs:* - Reports showing service demand, reports on peak usage times and attendance / no-show rates.
    * *Concerns:* - Maintaining compliance, protecting sensitive student data and resource allocation issues.
* **IT Administrator (Potential)**
    * *Needs:* - Centralised user role management and seamless integration with existing college authentication credentials.
    * *Concerns:* - Security vulnerabilities, data privacy and system reliability during peak periods.
* **Administrative Staff (Potential)**
    * *Needs:* - Ease of contact for all support departments and access to information on both the students and the support staff
    * *Concerns:* - Protecting sensitive student information, not having access to up-to-date information regarding the departments, keeping accurate records
* **Data Protection Contact (Potential)**
    * *Needs:* - Knowledge of exactly what information the system will require from its users 
    * *Concerns:* - Compliance with laws regarding personal user information, making sure of correct usage of sensitive data

## 2. Unknowns

**Who can use it?**
* Can a student hold more than one booking at once or book the same service repeatedly?
* What level of authorization is needed to book an appointment?

**The appointment itself**
* How many services are there, and what are they?
* What information does a student have to give when booking? Is there any optional information that is required?
* Are appointments only one-to-one or are there any group sessions?
* What shold happen if the slots are all full (a waiting list for example)?
* Are there different appointment types? (in person, online, phone etc.)?
* How are cancellations and no-shows handled?
* What is the minimum cancellation notice required before a student loses or frees up an appointment slot?

**Staff side**
* What happens to an existing booking when a staff member is sick or on leave?
* Can one advisor work across more than one service?
* How should the system fit with the calendars and spreadsheets staff already use, if at all?

**Information and privacy**
* What level of authorization is needed to handle booking cancellations / rescheduling?
* What data protectioin rules apply and who is responsible for the data?
* What credentials are currently used for the login sytem, and what rules apply when deciding the level of access granted with said credentials?
* How much student informatioin should administrative staff have access to compared to support staff?
* What student and appointment information does the college currently hold nd where is it stored?

**Accessibility and support**
* Do students with support needs require longer or priority slots?

**Constraints**
* Is there a budget, a deadline or a required technology?
* Are there rules about when a student may book, such as how far ahead or the maximum per term?

## 3. Information Sources

**Primary**

* Interviews with support advisors and service managers
* Interviews or a short survey with students who have already used support services
* A conversation with the college's data protection contact and IT administrator

**Secondary**
* Current calendars, spreadsheets and email or phone enquiry records
* College policies on data protection, accessibility and attendance
* The student handbook and service web pages, to see what the students are told now

## 4. Elicitation Questions

| **Who I'm asking** | **Unknown it answers** | **Type of question** | **The Question** |
| --- | --- | --- | --- |
| Students | Why they are unsure which service to contact | Problem | "Can you tell me about the last time you needed support from the college? How did you work out who to contact?" |
| Support Staff / Advisors | What happens to a booking when someone is sick or doesn't show | Exception | "Can you tell me about a time you couldn’t be at work when you had appointments booked? What happened to those appointments?" |
| Management | Rules on when and how often students may book | Information needed | "What limits or rules currently apply to how often or how far ahead a student can book a service?" |
| Data Protection Contact | What student and appointment information the college currently holds | Something we don't understand yet | "What information about students and their appointments does the college currently hold?" |
| Administrative Staff | How appointments are arranged today | Current process | "Can you walk me through how an appointment gets arranged today, from the moment a student first makes contact?" |
| IT Administrator | How the current login system handles credentials | Current process | "Can you walk me through what happens when a student or staff member logs into college systems and how it's decided what each person can access?" |

## 5. Candidate Requirement

### CR-F01 - The system shall allow authenticated students to search and view available support appointment slots by service type, advisor or date.

* **Source:** Initial discovery of the College Student Support Appointment Sytem scenario
* **Status:** Candidate - requires further investigation and validation
* **Elicitation needed:** We have to clarify which search options students need and whether all support services use the same appointment booking process
* **Stakeholders to ask:** Students and support staff / advisors

---
*[Back to top](#contents) | [Back to README](/README.md)*