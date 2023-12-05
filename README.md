# Standards

## API or WebServices Standards
* Guiding Principles:  Refer to www.soapprinciples.com to understand  _Stndardized Service Contract(agreement)_, _Service Loose Coupling (minimize the dependencies)_, _Service Abstraction (hide logic behind contract)_, _Service Reusability (dvide into smaller services to resuse)_, _Service Autonomy_, _Statelessness_, _Discoverability (metadata to discover and interpret)_, _Composability _
* Error Handling : Communicate Errors with Code, and Description/reason, message for Consumer
* API Endpoint URL:
  *   Focus on domain entities rather than the functions/algorithms,
  *   use Nouns over Verbs,
  *   Use Plurals for Resources (e.g. /api/v1/student-profileswith version)
* Gateway Tool (e.g. Apigee): Open API Specification, Proxy of actual functional API, Security policies (Keys,Secrets,IDs)
* Security: HTTPS/SSL for data encryption, No sensitive info (username,s passwords, session tokens, API keys) in endpoint URLs.
* Versioning: Revise Major version number when Response data format or type changes, and when API is removed.
* Headers: Include 'Name of the service' and 'Owner contact details for help'
* HTTP Methods:
  * GET: Retrieve one or more (read only) resouces, no Updates
  * POST: Create a new resources
  * PATCH, PUT, MERGET PATCH: To Update an existing resource (entire or partial)
  * DELETE: Used to delete existing resources (control with different privileges or separate this api from the rest)
  * Complex Queries: Use ? after the querystring to filter API collections/resource
* API Toggling: Toggle with HTTP Status Code 503
* Responses, Errors and Status Codes: Prefer successful responses in JSON format, Errors with Code, message, description
* Resource Mapping:
  * To _Create a resouce_: Use POST method, with _Create_ work in URL, other info request Body or headers
  * To _Get or Retrieve a resource_: Use POST method, Resouce ID in request Body
  * To _Update resource_: Use PUT method, resource attributes in request body
  * To _Delete a resouce_: Use Delete method, add 'Delete' keywork in URL, ResourceID in request Body.
* 
