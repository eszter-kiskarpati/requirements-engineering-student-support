# Agile Requirements - User Stories

## Contents

1. [User Stories](#1-user-stories)
2. [Open Questions](#2-open-questions)


*[Back to README](/README.md)*

## 1. User Stories

| Story ID / source requirement | User story | Acceptance criteria |
|---|---|---|
| **US-01** / FR-04, FR-18 (candidate) | As an authenticated student, I want to book an available appointment slot so that I can get help from a support service. | **Given** I am logged in and viewing an available slot for a support service, **when** I confirm the booking, **then** the appointment is recorded under my account.<br><br>**Given** I have confirmed a booking for a slot, **when** I or another student view that service's schedule, **then** that slot is no longer available to book. |
| **US-02** / FR-01 | As an authenticated student, I want to view available appointment slots for a support service so that I can choose a time that suits me. | **Given** I am logged in and select a support service, **when** the schedule loads, **then** all currently available slots for that service are displayed.<br><br>**Given** multiple support services have available slots, **when** I select one service, **then** only slots belonging to that chosen service are displayed. |
| **US-03** / FR-03 | As a student, I want to read a description of each support service so that I can decide which service fits my needs. | **Given** I am viewing the list of support services, **when** I check a service, **then** its description is displayed.<br><br>**Given** I am viewing a service's available appointments page, **when** I look at the service details, **then** the same service description is visible before I book. |
| **US-04** / FR-07, BR-02 (Candidate) | As an authenticated student, I want to cancel an existing appointment so that I can free up the time slot if I can no longer attend. | **Given** I am logged in and have a booked appointment, **when** I cancel that appointment, **then** the booking is removed from my active appointments.<br><br>**Given** I have cancelled my appointment, **when** students view that service's schedule, **then** the slot becomes available to book again. |
| **US-05** / FR-10 | As an authorised support staff member, I want to set my available appointment slots so that students can book times when I am free. | **Given** I am logged in as authorised support staff, **when** I add available appointment slots for my service, **then** those slots are saved.<br><br>**Given** I have saved new available slots, **when** an authenticated student views that support service, **then** the new slots appear as available to book. |

## 2. Open Questions

| Question | Related story / requirement |
|---|---|
| Are there any booking limits per student (for example, can a student book more than one appointment at a time or a second appointment with the same service)? | US-01 / FR-04 |
| Is there a cut-off window before an appointment starts (e.g. 24 hours in advance) after which a student can no longer cancel? | US-04 / FR-07 |

---
*[Back to top](#contents) | [Back to README](/README.md)*