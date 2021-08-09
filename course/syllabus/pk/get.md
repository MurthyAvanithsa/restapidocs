# Show Single Syllabus item

Show a single Syllabus item if current User has access permissions to it.

**URL** : `/api/syllabus/:pk/`

**URL Parameters** : `pk=[integer]` where `pk` is the ID of the Syllabus item on the
server.

**Method** : `GET`

**Auth required** : YES

**Data**: `{}`

## Success Response

**Condition** : If Syllabus item exists and Authorized User has required permissions.

**Code** : `200 OK`

**Content example**

```json
{
  "id": 345,
  "name": "Week1",
  "description": "Learn python basics.",
  "url": "http://testserver/api/syallbus/345/"
}
```

## Error Responses

**Condition** : If Syllabus item does not exist with `id` of provided `pk` parameter.

**Code** : `404 NOT FOUND`

**Content** : `{}`

### Or

**Condition** : If Syllabus item exists but Authorized User does not have required
permissions.

**Code** : `403 FORBIDDEN`

**Content** :

```json
{ "detail": "You do not have permission to perform this action." }
```

## Notes

There are security issues:

- This view allows existing users to test for existence of Syllabus items that exist
  but that they do not have access to.
- Syllabus item IDs are sequential so an authorized user can count all the Syllabus items
  on the system.
