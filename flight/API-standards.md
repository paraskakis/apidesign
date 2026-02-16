# API Standards

## Guidelines:
1. Default to a HTTP REST API unless otherwise specified.
2. Follow Joshua Bloch’s principles in “How to Design a Good API and Why it Matters”: https://static.googleusercontent.com/media/research.google.com/en//pubs/archive/32713.pdf
   * Characteristics of a good API:
   * Easy to learn
   * Easy to use, even without documentation
   * Hard to misuse
   * Easy to read and maintain code that uses it
   * Sufficiently powerful to satisfy requirements
   * Easy to extend
   * Appropriate to audience

## Standards:
Follow all the standards below — do not skip any of them.
Default to HTTP standards as found in the following RFCs:
https://www.rfc-editor.org/rfc/rfc9110
https://www.rfc-editor.org/rfc/rfc9112
https://www.rfc-editor.org/rfc/rfc9113
https://www.rfc-editor.org/rfc/rfc9114

### Style Guide:
Follow API industry accepted standards, conventions and best practices.

### Requests:
All requests must use JSON.

### Responses:
All responses must use JSON.

### Naming Conventions:
1. Use clear naming and employ suggestions from schema repositories such as schema.org, GS1, ISO, and similar vertical industry standards.
2. Follow industry standards, including RFCs, IANA, and JSON Schema for naming and definitions.
3. Avoid abbreviations except where they are very well known - for example, `ID` is ok and preferred over `identifier`.

### Paths:
1. Do not use /api as a base path unless specified.
2. Do not put a version number like /v1 in the path unless specified.

### Resources:
1. Pluralize resource names.
2. You should nest resources to follow object relations, but not more than 3 levels. If an object is a child object of another, it should be nested - for example, `projects/{id}/tasks`.

### Properties:
1. Use camelCase for field names.
2. If possible, use enums over strings.

### Query Parameters:
1. Use lowercase and don;t depend on casing.

### Security:
1. Always implement authentication unless your input indicates otherwise.
2. If the authentication method is not obvious, ask the user to specify the desired type (e.g., API Key, OAuth 2.0, etc.) using only security schemes supported by OpenAPI.
3. If using API Key, ensure you use `Authorization` as a header, not `X-Api-Key`.
4. Follow best practices as outlined in OWASP API Top-10 - https://owasp.org/www-project-api-security/
5. Document 401 (Unauthorized) responses for endpoints requiring authentication.
6. Prefer API Key over Bearer authentication if there are no further instructions.
7. Never use Basic Auth

### IDs:
Use UUIDs throughout for all resource identifiers, unless otherwise specified for each resource in requirements - Follow https://www.rfc-editor.org/rfc/rfc9562.html

### Dates:
Use ISO 8601 Dates - Follow https://datatracker.ietf.org/doc/html/rfc3339 &  https://datatracker.ietf.org/doc/html/rfc9557

### Parameters:
1. Use pagination for all collection endpoints. Use offset and limit unless otherwise specified.

### Errors:
1. Document all possible error conditions.
2. Use the Problem Details format to describe error responses as described in https://www.rfc-editor.org/rfc/rfc9457.html

### Status Codes:
1. Use status codes 200, 201, 202 and 204 appropriately for successful responses.
2. Include a 404 status code for resources not found.
3. Include a 401 status code for endpoints requiring authentication.
4. Use 500 status codes for server errors.
5. Use 429 status codes to indicate rate-limiting issues.

### Rate Limiting:
1. Include standard Rate Limiting Headers for successful (200, 201, 202, 204) responses, such as X-RateLimit-Limit, X-RateLimit-Remaining, and Retry-After.
2. Also include standard Rate Limiting Headers for 400, 401, 403, 404 and other 4XX responses.
