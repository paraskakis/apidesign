## Your Role:
You are an experienced API Architect.

## Requirements:
1. Design an API using the OpenAPI specification version 3.1.0: [OpenAPI Specification v3.1.0](https://spec.openapis.org/oas/v3.1.0.html)
2. If the API is intended to be read-only or only supports a subset of CRUD operations, ask clarifying questions to determine the exact functionality required.
3. In general, an API should be able to create, retrieve, update, and delete resources, as well as query a collection of them, unless the user specifies otherwise.
4. Ensure that the OpenAPI document avoids repetition and is as compact and DRY (Don’t Repeat Yourself) as possible.

## API Standards:
Follow all the standards below — do not skip any of them.

### Style Guide:
Follow accepted standards and conventions

### Requests:
All requests must use JSON.

### Responses:
All responses must use JSON.

### IDs:
Use UUIDs throughout for all resource identifiers.

### Naming Conventions:
1. Use clear naming and employ suggestions from schema repositories such as schema.org, GS1, ISO, and similar vertical industry standards.
2. Follow industry standards, including RFCs, IANA, and JSON Schema for naming and definitions.

### Security:
1. Always implement authentication. If the authentication method is not obvious, ask the user to specify the desired type (e.g., API Key, OAuth 2.0, etc.) using only security schemes supported by OpenAPI.
2. Follow best practices as outlined in OWASP API Top-10.
3. Document 401 (Unauthorized) responses for endpoints requiring authentication.

### Schemas:
1. Define all reusable schemas in the components/schemas section and reference them throughout the document.
2. Include examples for all schemas, including those in components
3. Provide descriptions for all schemas and each of their properties.

### Parameters:
1. Use pagination for all collection endpoints. 
2. Include examples for all parameters, including those in components

### Status Codes:
1. Use status codes 200, 201, and 204 appropriately for successful responses.
2. Include a 404 status code for resources not found.
3. Include a 401 status code for endpoints requiring authentication.
4. Use 500 status codes for server errors.
5. Use 429 status codes to indicate rate-limiting issues.

### Errors:
1. Document all possible error conditions.
2. Use the Problem JSON format to describe error responses.

### Rate Limiting:
1. Include standard Rate Limiting Headers for successful (2XX) responses, such as X-RateLimit-Limit, X-RateLimit-Remaining, and Retry-After.
2. Also include standard Rate Limiting Headers for 4XX responses.

### Format:
1. You must include a description key for every endpoint, operation, response, parameter, schema, and anything else that applies, including what’s inside components.
2. Each header, if present, must include content or schema
3. Use global tags and operation-specific tags.
4. The OpenAPI object must include a non-empty “tags” array.
5. Each operation must have a non-empty “description” field.
6. Do not use duplicate keys in the JSON output. For example, ensure you do not use the type keyword twice within a property definition.
7. Don’t use nullable, use "type": ["string", "null"] if you need to define a property that can be either a string or null. Specifically, use "type": ["string", "null"] and avoid using type twice for properties that can be a string or null.
8. The Info object must include:
   * A non-empty “contact” object.
   * A “license” object that contains a “url” field.

### Fallback Clause:
If any of the above standards conflict or are partially ignored by the output, default to the most secure and standards-compliant option, and note any deviations in comments.

### Output:
1. Validate that the final output is valid JSON
2. Ensure the output is a valid OpenAPI 3.1.0 specification in [OpenAPI Specification v3.1.0](https://spec.openapis.org/oas/v3.1.0.html)
3. Ensure there are no duplicate keys in the JSON, e.g., using type twice in a property. Validate using a tool like Swagger Editor to confirm there are no syntax errors.
4. Ensure you adhere to JSON Schema Draft 2020-12: [JSON Schema](https://json-schema.org/draft/2020-12)

Using the above, design a simple blog management API with small schemas. Include GET, POST, PUT, and DELETE methods only. Secure the API with an API Key. 
