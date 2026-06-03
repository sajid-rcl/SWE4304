# Relationships and Cardinalities

## 1:N Relationships

### Division → ProgrammeWorkshop
A division can manage many programmes/workshops, but each programme/workshop belongs to one division.

```text
Division 1 —— N ProgrammeWorkshop
```

### AccreditingBody → ProgrammeWorkshop
An accrediting body can accredit many programmes/workshops, but each programme/workshop has one accrediting body.

```text
AccreditingBody 1 —— N ProgrammeWorkshop
```

### Campus → Session
A campus can host many sessions, but each session takes place at one campus.

```text
Campus 1 —— N Session
```

### ProgrammeWorkshop → Session
One programme/workshop can have many sessions, but each session belongs to one programme/workshop.

```text
ProgrammeWorkshop 1 —— N Session
```

### Instructor → Session
One instructor can teach many sessions, but each session has one instructor.

```text
Instructor 1 —— N Session
```

### Session → Enrolment
One session can have many enrolments, but each enrolment belongs to one session.

```text
Session 1 —— N Enrolment
```

### Campus → Instructor
One campus can have many instructors, but each instructor has one home campus.

```text
Campus 1 —— N Instructor
```

---

# N:1 Relationships

## ProgrammeWorkshop → Division

```text
ProgrammeWorkshop N —— 1 Division
```

## ProgrammeWorkshop → AccreditingBody

```text
ProgrammeWorkshop N —— 1 AccreditingBody
```

## Session → Campus

```text
Session N —— 1 Campus
```

## Session → ProgrammeWorkshop

```text
Session N —— 1 ProgrammeWorkshop
```

## Session → Instructor

```text
Session N —— 1 Instructor
```

## Enrolment → Session

```text
Enrolment N —— 1 Session
```

## Instructor → Campus

```text
Instructor N —— 1 Campus
```

---

# M:N Relationships

## Participant ↔ Session
A participant can register for many sessions, and a session can have many participants.

```text
Participant M —— N Session
```

Resolved using the Enrolment entity:

```text
Participant 1 —— N Enrolment N —— 1 Session
```

---

# 1:1 Relationships

There is no mandatory 1:1 relationship explicitly defined in the requirements.

Possible optional example:

## Division ↔ HeadOfDivision

```text
Division 1 —— 1 HeadOfDivision
```

(Only if HeadOfDivision is treated as a separate entity rather than an attribute.)
