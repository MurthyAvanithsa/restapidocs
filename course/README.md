# RESTAPIDocs Examples

These examples were taken from projects mainly using [Django Rest
Framework](https://github.com/tomchristie/django-rest-framework) and so the
JSON responses are often similar to the way in which DRF makes responses.

Where full URLs are provided in responses they will be rendered as if service
is running on 'http://testserver/'.

## Open Endpoints

Open endpoints require no Authentication.

- [Login](login.md) : `POST /api/login/`

## Endpoints that require Authentication

Closed endpoints require a valid Token to be included in the header of the
request. A Token can be acquired from the Login view above.

### Syllabus related

Endpoints for viewing and manipulating the Accounts that the Authenticated User
has permissions to access.

- [Show all syllabus items](syllabus/get.md) : `GET /api/course/`
- [Create syllabus](syllabus/post.md) : `POST /api/syllabus/`
- [Show An syllabus](syllabus/pk/get.md) : `GET /api/syllabus/:pk/`
- [Update An syllabus](syllabus/pk/put.md) : `PUT /api/syllabus/:pk/`
- [Delete An syllabus](syllabus/pk/delete.md) : `DELETE /api/syllabus/:pk/`
