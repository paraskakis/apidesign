# Conference Domain

## Domain Description:
* A Conference has Tracks (thematic groupings like "API Design" or "AI/ML").
* A Track contains Talks. A Talk is a session delivered by a speaker at a scheduled time in a room.

## Data Objects and Properties:

### Track
- ID (string, UUID) - required
- Name (string) - example: "OpenAPI Summit" - required
- Description (string) - required

### Speaker
- ID (string, UUID) - required
- Name (string) - example: "Emmanuel Paraskakis" - required
- Title (string) - example: "API Consultant" - required
- Company (string) - example: "Level 250"
- Bio (string) - example: "API consultant and educator specializing in API strategy and design"

### Talk
- ID (string, UUID) - required
- Title (string) - example: "AI-Driven API Design with OpenAPI" - required
- Description (string) - required
- Format (enum: Keynote, Talk, Workshop, Panel) - example: "Talk" - required
- Room (string) - example: "PRO Stage" - required
- TrackID (string, UUID, reference to Track) - required
- SpeakerIDs (array of string, UUIDs, references to Speaker) - required
- Date (date, RFC3339/ISO8601) - example: "2026-02-20" - required
- StartTime (datetime, RFC3339/ISO8601 UTC) - example: "2026-02-20T21:30:00Z" - required
- EndTime (datetime, RFC3339/ISO8601 UTC) - example: "2026-02-20T22:15:00Z" - required

## Object Relations:
1. A Track has many Talks.
2. A Talk belongs to exactly one Track.
3. A Talk has one or more Speakers.
4. A Speaker may have multiple Talks.
