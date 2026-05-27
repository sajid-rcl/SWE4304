# Activity C – Draft Business Rules and Candidate Entities

## Business Rules

1. A division can manage many programmes and workshops.
2. Each programme or workshop belongs to one division only.
3. An accrediting body can accredit many programmes or workshops.
4. Each programme or workshop may be accredited by one accrediting body.
5. A programme or workshop can have many sessions.
6. Each session belongs to one programme or workshop.
7. Each session is delivered by one instructor.
8. An instructor can deliver many sessions.
9. Each instructor has one home campus.
10. A campus can host many sessions.
11. A participant can enrol in many sessions.
12. Each enrolment links one participant to one session.

---

# Candidate Entities and Key Attributes

## Division
- DivisionID (PK)
- DivisionName
- HeadOfDivision
- ContactInfo

## Programme
- ProgrammeID (PK)
- ProgrammeCode
- ProgrammeTitle
- ProgrammeType
- AccreditingBodyID (FK)
- DivisionID (FK)

## Workshop
- WorkshopID (PK)
- WorkshopTitle
- WorkshopType
- AccreditingBodyID (FK)
- DivisionID (FK)

## AccreditingBody
- AccreditingBodyID (PK)
- AccreditingBodyName
- Address
- ContactInfo

## Session
- SessionID (PK)
- SessionDate
- SessionTime
- Location
- CampusID (FK)
- InstructorID (FK)

## Campus
- CampusID (PK)
- CampusName
- Address
- Capacity

## Instructor
- InstructorID (PK)
- InstructorName
- Qualifications
- HomeCampusID (FK)

## Participant
- ParticipantID (PK)
- ParticipantName
- Email
- PhoneNumber

## Enrolment
- EnrolmentID (PK)
- EnrolmentDate
- ParticipantID (FK)
- SessionID (FK)

---

# Uncertainties / Questions

1. Should Programme and Workshop be separate entities or combined into one entity with a type attribute?
2. Can a session be delivered by more than one instructor?
3. Can a programme or workshop have multiple accrediting bodies?
4. Should participant payment details be included in the database?
5. Can sessions be delivered online as well as on campus?
