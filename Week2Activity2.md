# Activity D – ERD v0.1 Workshop

## ERD v0.1 – Entities

1. Division
2. Programme
3. AccreditingBody
4. Session
5. Instructor
6. Campus
7. Participant
8. Enrolment

---

# Relationships with Cardinality and Optionality

| Relationship | Cardinality | Optionality |
|---|---|---|
| Division manages Programme | 1 : Many | Mandatory for Programme |
| AccreditingBody accredits Programme | 1 : Many | Optional for Programme |
| Programme has Session | 1 : Many | Mandatory for Session |
| Instructor delivers Session | 1 : Many | Mandatory for Session |
| Campus hosts Session | 1 : Many | Mandatory for Session |
| Participant registers through Enrolment | 1 : Many | Optional for Participant |
| Session linked through Enrolment | 1 : Many | Mandatory for Enrolment |

---

# Business Rules

1. A division can manage many programmes.
2. Each programme belongs to one division only.
3. An accrediting body can accredit many programmes.
4. A programme may be accredited by one accrediting body.
5. A programme can have many sessions.
6. Each session belongs to one programme.
7. Each session is delivered by one instructor.
8. An instructor can deliver many sessions.
9. A campus can host many sessions.
10. Each session takes place at one campus.
11. A participant can enrol in many sessions.
12. Each enrolment links one participant to one session.

---

# Assumptions + Questions

1. Programmes and workshops are treated as a single entity using a type attribute.
2. Each session is taught by only one instructor.
3. Participants can enrol in multiple sessions.
4. A session cannot exist without a programme.
5. Online sessions are currently excluded from the system.
6. Should cancelled enrolments be stored in the database?
7. Can instructors belong to more than one campus?
8. Should workshop attendance records be included?
9. Can a programme have multiple accrediting bodies?
10. Should participant payment information be part of the database?

---

# Glossary

| Term | Definition |
|---|---|
| Entity | A real-world object stored in the database. |
| Attribute | A property describing an entity. |
| Relationship | An association between two entities. |
| Primary Key (PK) | A unique identifier for each record. |
| Foreign Key (FK) | An attribute linking related tables. |
| Cardinality | Defines the number of relationships between entities. |
| Optionality | Indicates whether participation in a relationship is optional or mandatory. |
| Constraint | A rule that ensures valid and consistent data. |
| ERD | Entity Relationship Diagram used to model databases. |
| Normalisation | Process of reducing redundancy in database tables. |

---

# Deliverables

- ERD export in PNG or PDF format
- MySQL Workbench `.mwb` file
- Business rules list
- Glossary of key database terms
