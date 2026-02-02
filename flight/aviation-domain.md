# Aviation Domain

## Domain Description:
* The aviation domain consists of data needed to track aviation movements in the past, present, and future.
* Organizations operate aircraft. Organizations MAY be Airlines or other entities.
* Aircraft travel from the Departure Airport to the Destination Airport along a Route. This is called a Flight, and it occurs on a specific Date.

## Data Objects and Properties:

### **Note on Identifiers:**
1. An airport's unique ID is the ICAO ID, not a UUID.
2. A Flight is identified by a combination of Identifier and Date which is what makes it unique. This is a composite key, meaning that both are required - the first part is the Flight Identifier, and within that, the Date.

### Airport
- ID (string, ICAO unique identifier) - example: "KSFO" - required - **NOTE: not UUID**
- Code (string, IATA unique identifier) - example: "SFO" - required
- Name (string) - example: “San Francisco International Airport” - required
- City (string) - example: "San Francisco" - required
- Country (string, two English alphabet letters, ISO 3166-1 A2) - example: "US" - required
- Airport Reference Point Lattitude (number, Lattitude in WGS 84 system) - example: 37.61881 - required
- Airport Reference Point Longitude (number Longitude in WGS 84 system) - example: -122.37542 - required
- Elevation (integer) - feet above Mean Sea Level - example: 13 - required


### Flight
- Identifier (string) - example: "EK225" **NOTE: not UUID - A Flight's ID is the Identifier + Date Below concatenated, a composite key - maintain both fields separately as well as the concatenated ID** - required
- Date (date, RFC3339/ISO8601 UTC) - example: "2026-02-01T21:07:42Z" - required
- Aircraft Type (string, ICAO DOC8643) - example: "A388" - required
- Aircraft Registration (string, valid ICAO registration) - example: "A6-EOM"
- Number (number, 2 digits) - example: 01 - required
- Flight Rules (enum: I, V, Y, Z) - example: I - required
- Flight Type (enum S, N, G, M, X) - example: S - required
- Departure Airport (string, ICAO unique identifier) - example: "OMDB" - required
- Destination Airport (string, ICAO unique identifier) - example: "KSFO" - required
- Planned Time of Departure (date, RFC3339/ISO8601 UTC) - example: "2026-02-01T21:07:42Z" - required
- Estimated Time of Departure (date, RFC3339/ISO8601 UTC) - example: "2026-02-01T21:07:42Z"
- Actual Time of Departure (date, RFC3339/ISO8601 UTC) - example: "2026-02-01T21:07:42Z"
- Estimated Time Enroute (integer, time in minutes) - example: 960 - required
- Estimated Time of Arrival (date, RFC3339/ISO8601 UTC) - example: "2026-02-02T21:07:42Z"
- Actual Time of Arrival (date, RFC3339/ISO8601 UTC) - example: "2026-02-02T21:07:42Z"
- Route (string) - example: "OMDB KSFO" - required
- Current Speed (number, knots) - example: 0
- Current Heading (number magnetic) - example: 270
- Current Level (number, Flight Level) - example: 0
- Current Position Lattitude (number, Lattitude in WGS 84 system) - example: 37.61881
- Current Position Longitude (number Longitude in WGS 84 system) - example: -122.37542


## Object Relations:
1. A Flight MAY Depart and Arrive at the same Airport
2. A Flight MUST be uniquely identified by Identifier + Date (composite key)
3. There MAY be many Flights between Airport pairs, but there MUST be only one for that Identifier + Date combination
4. An Identifier MAY include an Organization Code, for a example for a particular Airline
