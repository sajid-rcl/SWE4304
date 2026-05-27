# Cardinality and Participation Constraints

## Division → ProgrammeWorkshop
```text
Division 1..1 —— 1..* ProgrammeWorkshop
```

## AccreditingBody → ProgrammeWorkshop
```text
AccreditingBody 1..1 —— 0..* ProgrammeWorkshop
```

## Campus → Session
```text
Campus 1..1 —— 0..* Session
```

## ProgrammeWorkshop → Session
```text
ProgrammeWorkshop 1..1 —— 1..* Session
```

## Instructor → Session
```text
Instructor 1..1 —— 0..* Session
```

## Campus → Instructor
```text
Campus 1..1 —— 0..* Instructor
```

## Session → Enrolment
```text
Session 1..1 —— 0..* Enrolment
```

## Participant → Enrolment
```text
Participant 1..1 —— 0..* Enrolment
```

# Many-to-Many Relationship

## Participant ↔ Session
```text
Participant 0..* —— 0..* Session
```

## Resolved Using Associative Entity
```text
Participant 1..1 —— 0..* Enrolment 0..* —— 1..1 Session
```
