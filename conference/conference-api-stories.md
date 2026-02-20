# Conference Schedule API — User Stories

## Tracks

**List all tracks**
As an attendee, I want to browse all conference tracks so I can understand the thematic areas and plan my schedule.
`GET /tracks` — params: `offset`, `limit`

**Get a track**
As an attendee, I want to view a specific track's details so I can decide if it's relevant to my interests.
`GET /tracks/{trackId}`

**List talks in a track**
As an attendee, I want to see all talks within a track so I can find sessions on a topic I care about.
`GET /tracks/{trackId}/talks` — params: `offset`, `limit`, `format`, `date`

---

## Talks

**List all talks**
As an attendee, I want to browse all talks across the conference so I can build my personal schedule.
`GET /talks` — params: `offset`, `limit`, `format`, `date`, `trackId`

**Get a talk**
As an attendee or speaker, I want to view a specific talk's full details — description, room, time, and speaker — so I know exactly where to be and what to expect.
`GET /talks/{talkId}`

---

## Speakers

**List all speakers**
As an attendee, I want to browse and search for speakers by name so I can quickly find someone I'm looking for without scrolling through the full list.
`GET /speakers` — params: `offset`, `limit`, `name`

`name` is a case-insensitive partial match string (e.g., `?name=emma` returns "Emmanuel Paraskakis").

**Get a speaker**
As an attendee, I want to view a speaker's profile and background so I can decide whether to prioritize their session.
`GET /speakers/{speakerId}`

**List talks by a speaker**
As an attendee or speaker, I want to see all talks a specific speaker is giving so I can follow their content or check my own schedule.
`GET /speakers/{speakerId}/talks` — params: `offset`, `limit`

---

## Notes

- **No authentication** — all endpoints are public, no auth required.
- **No versioning or `/api` prefix.**
- **`format` filter** is an enum (Keynote, Talk, Workshop, Panel) across talk collection endpoints.
- **`date` filter** uses ISO 8601 format (e.g., `2026-02-20`) for multi-day conference browsing.
- **`trackId` filter on `/talks`** provides a flat alternative to the nested route, useful for third-party app developers.
