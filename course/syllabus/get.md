# Show Syllabus items

Show all Syllabus items the active User can access.

**URL** : `/api/syllabus/`

**Method** : `GET`

**Auth required** : YES

**Permissions required** : None

**Data constraints** : `{}`

## Success Responses

**Code** : `200 OK`

**Content** : `{[]}`

**Content** : In this example, the syllabus items can see

```json
[
  {
    "id": 345,
    "name": "Week1",
    "description": "Learn python basics.",
    "url": "http://testserver/api/syallbus/345/"
  },
  {
    "id": 346,
    "name": "Week2",
    "description": "Database interaction with python.",
    "url": "http://testserver/api/syallbus/345/"
  }
]
```
