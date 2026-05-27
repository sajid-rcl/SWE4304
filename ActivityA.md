# SWE4304 Databases – Assignment 1 Brief

## Scope Statement

### In Scope
The proposed database system will manage the administration of Regent College London’s professional training and short course division. The system will store and manage information about divisions, programmes, workshops, accrediting bodies, campuses, instructors, sessions, and participant enrolments. It will support scheduling sessions across multiple campuses, assigning instructors, and tracking participant registrations for each session.

### Out of Scope
The system will not manage student academic grades, tuition fee payments, payroll, HR records, or online learning platforms. It will also exclude advanced analytics, attendance tracking, and automated email notification features. The database is intended only for operational management and reporting related to training programmes and workshops.

---

## Assumptions

1. Each programme or workshop belongs to only one division.
2. Each instructor has one home campus but may teach sessions at different campuses.
3. A participant can enrol in multiple sessions, but each enrolment record refers to one session only.
4. Each session is delivered by one instructor at one campus location.
5. Accrediting bodies may accredit multiple programmes or workshops.

---

## Candidate Entities

The following candidate entities were identified from the business scenario:

1. Division
2. Programme
3. Workshop
4. Accrediting Body
5. Session
6. Campus
7. Instructor
8. Participant
9. Enrolment

---

## Notes for Peer Feedback

For peer feedback, I would like comments on:

- Whether the identified entities are appropriate and complete.
- Whether the scope is realistic and clearly defined.
- If any assumptions should be added, removed, or clarified.
- Whether Programme and Workshop should remain separate entities or be combined into one entity with a type attribute.
