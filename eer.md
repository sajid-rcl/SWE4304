# 1 : 1 Relationships

There are no true **1 : 1** relationships in this model.

---

# 1 : M Relationships

## Division → ProgrammeWorkshop
Division 1..1 —— 1..* ProgrammeWorkshop

- One Division can have many ProgrammeWorkshops.
- Each ProgrammeWorkshop belongs to exactly one Division.

---

## AccreditingBody → ProgrammeWorkshop
AccreditingBody 1..1 —— 0..* ProgrammeWorkshop

- One AccreditingBody can accredit many ProgrammeWorkshops.
- Each ProgrammeWorkshop belongs to one AccreditingBody.

---

## Campus → Session
Campus 1..1 —— 0..* Session

- One Campus can host many Sessions.
- Each Session belongs to one Campus.

---

## ProgrammeWorkshop → Session
ProgrammeWorkshop 1..1 —— 1..* Session

- One ProgrammeWorkshop can contain many Sessions.
- Each Session belongs to one ProgrammeWorkshop.

---

## Instructor → Session
Instructor 1..1 —— 0..* Session

- One Instructor can teach many Sessions.
- Each Session is taught by one Instructor.

---

## Campus → Instructor
Campus 1..1 —— 0..* Instructor

- One Campus can have many Instructors.
- Each Instructor belongs to one Campus.

---

## Session → Enrolment
Session 1..1 —— 0..* Enrolment

- One Session can have many Enrolments.
- Each Enrolment belongs to one Session.

---

## Participant → Enrolment
Participant 1..1 —— 0..* Enrolment

- One Participant can have many Enrolments.
- Each Enrolment belongs to one Participant.

---

# M : N Relationships

## Participant ↔ Session
Participant 0..* —— 0..* Session

- One Participant can attend many Sessions.
- One Session can contain many Participants.

This is a many-to-many (M:N) relationship.

---

# M : N Relationship Resolved Using Associative Entity

## Using Enrolment
Participant 1..1 —— 0..* Enrolment 0..* —— 1..1 Session

- Enrolment acts as the associative entity.
- The original M:N relationship between Participant and Session is resolved into two 1:M relationships.
