# Delete Syllabus item

Delete the Account of the Authenticated User if they are Owner.

**URL** : `/api/syllabus/:pk/`

**URL Parameters** : `pk=[integer]` where `pk` is the ID of the syllabus item in the
database.

**Method** : `DELETE`

**Auth required** : YES

**Data** : `{}`

## Success Response

**Condition** : If the item exists.

**Code** : `204 NO CONTENT`

**Content** : `{}`

## Error Responses

**Condition** : If there was no syllabus item available to delete.

**Code** : `404 NOT FOUND`

**Content** : `{}`

### Or

**Condition** : User is not Authorized .

**Code** : `403 FORBIDDEN`

**Content** : `{}`
