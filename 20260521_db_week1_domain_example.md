# Professional Conference Management System

## Scenario

A professional training company manages conferences, seminars, and workshops across multiple venues in the UK. The organisation needs a database system to manage events, speakers, venues, sponsors, and attendee registrations.

The system should support:
- Managing organisations and conference providers
- Organising conferences and seminars
- Assigning speakers to sessions
- Managing venues and halls
- Tracking attendee registrations
- Recording sponsor information

---

# Candidate Entities

- Organisation
- Conference
- Sponsor
- EventSession
- Venue
- Speaker
- Registration

---

# Example Tables and Sample Data

## Organisations

| organisation_id | organisation_name      | manager_name   | contact_email                  |
|---|---|---|---|
| ORG001 | TechSkills Academy | Sarah Ahmed | info@techskills.com |
| ORG002 | FutureLearn Hub | Daniel Smith | contact@futurelearnhub.com |

---

## Conferences

| conference_code | title | category | organisation_id |
|---|---|---|---|
| CONF101 | Cloud Computing Bootcamp | Technology | ORG001 |
| CONF102 | Agile Project Management | Business | ORG002 |

---

## Sponsors

| sponsor_id | sponsor_name | address | contact_number |
|---|---|---|---|
| SP001 | Innovate UK | London | 0201234567 |
| SP002 | DataCore Ltd | Manchester | 0161987654 |

---

## EventSessions

| session_id | session_date | session_time | hall | speaker_id |
|---|---|---|---|---|
| SES001 | 2026-07-10 | 10:00 | Hall A | SPE001 |
| SES002 | 2026-07-11 | 14:00 | Hall B | SPE002 |

---

## Venues

| venue_id | venue_name | address | seating_capacity |
|---|---|---|---|
| VEN001 | Manchester Conference Centre | Manchester | 300 |
| VEN002 | London Tech Hall | London | 500 |

---

## Speakers

| speaker_id | speaker_name | expertise | affiliated_organisation |
|---|---|---|---|
| SPE001 | John Carter | Cloud Computing | TechSkills Academy |
| SPE002 | Emily Brown | Agile Methodologies | FutureLearn Hub |

---

## Registrations

| registration_id | attendee_name | attendee_email | session_id |
|---|---|---|---|
| REG001 | Ali Hassan | ali@email.com | SES001 |
| REG002 | Maria Khan | maria@email.com | SES002 |

---

# Example Relationships

- Organisation manages Conference
- Conference contains EventSession
- Speaker delivers EventSession
- Venue hosts EventSession
- Attendee registers for EventSession
- Sponsor supports Conference

---

# Example Assumptions

1. Each conference belongs to one organisation.
2. Each session is delivered by one speaker.
3. A venue can host multiple sessions.
4. A participant can register for multiple sessions.
5. Each sponsor can support multiple conferences.

---

# Example Scope Statement

## In Scope
- Conference management
- Speaker management
- Session scheduling
- Registration tracking
- Venue management

## Out of Scope
- Online payments
- Accommodation booking
- Transport management
- Video streaming services