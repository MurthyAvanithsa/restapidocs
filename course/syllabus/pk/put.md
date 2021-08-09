# Update Syllabus item

Update the syllabus item.

**URL** : `/api/syllabus/:pk/`

**Method** : `PUT`

**Auth required** : YES

**Data constraints**

```json
{
  "name": "[unicode 64 chars max]"
}
```

**Data example** Partial data is allowed, but there is only one field.

```json
{
  "name": "Build something project dot com"
}
```

## Success Responses

**Condition** : Update can be performed either fully or partially by the Owner
of the Account.

**Code** : `200 OK`

**Content example** : For the example above, when the 'name' is updated and
posted to `/api/accounts/123/`...

```json
{
  "id": 345,
  "name": "Week1",
  "description": "Learn python basics.",
  "url": "http://testserver/api/syallbus/345/"
}
```

## Error Response

**Condition** : Syllabus does not exist at URL

**Code** : `404 NOT FOUND`

**Content** : `{}`

### Or

**Condition** : Authorized User is not Owner of Account at URL.

**Code** : `403 FORBIDDEN`

**Content** : `{}`

## Notes

### Data ignored

Endpoint will ignore irrelevant and read-only data such as parameters that
don't exist, or `id` and `enterprise` fields which are not editable.
