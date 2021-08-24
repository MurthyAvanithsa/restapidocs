# Create Syllabus item

Create an syllabus item.

**URL** : `/api/syllabus/`

**Method** : `POST`

**Auth required** : YES

**Permissions required** : None

**Data constraints**

Provide name of Account to be created.

```json
{
  "name": "[unicode 64 chars max]",
  "description": "[unicode 64 chars max]",
  "learningObjectives": "[csv of string]"
}
```

**Data example** All fields must be sent.

```json
{
  "id": 345,
  "name": "Week1",
  "description": "Learn python basics.",
  "url": "http://testserver/api/syallbus/345/"
}
```

## Success Response

**Condition** : If everything is OK and an Account didn't exist for this User.

**Code** : `201 CREATED`

**Content example**

```json
{
  "id": 123,
  "name": "Build something project dot com",
  "learningObjectives": "MYSQL,SQL"
}
```

### Or

**Condition** : If fields are missed.

**Code** : `400 BAD REQUEST`

**Content example**

```json
{
  "name": ["This field is required."]
}
```
