---
title: "Remove a student"
description: "Removes an educationUser from an educationClass"
---

# Remove a student

> **Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change. Use of these APIs in production applications is not supported.

Removes an [educationUser](../resources/educationuser.md) from an [educationClass](../resources/educationclass.md)

>**Note:** Teachers _and_ students are in the class **members** collection. Before calling this API, insure that the **educationUser** you are removing is not a teacher.  Get the list of teachers by calling [educationclass_list_teachers](educationclass-list-teachers.md) and verifying the user Id of the user to be removed is not in the returned teacher list.

## Permissions
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

|Permission type      | Permissions (from least to most privileged)              |
|:--------------------|:---------------------------------------------------------|
|Delegated (work or school account) |  Not supported.  |
|Delegated (personal Microsoft account) |  Not supported.  |
|Application | EduRoster.ReadWrite.All | 

## HTTP request
<!-- { "blockType": "ignored" } -->
```http
DELETE /education/classes/{id}/members/{userId}/$ref
```
## Request headers
| Header       | Value |
|:---------------|:--------|
| Authorization  | Bearer {token}. Required.  |

## Request body
Do not supply a request body for this method.


## Response
If successful, this method returns a `204 No Content` response code and an empty response body.

## Example
##### Request
The following is an example of the request.
<!-- {
  "blockType": "request",
  "name": "create_educationclass_from_educationschool"
}-->
```http
DELETE https://graph.microsoft.com/beta/education/classes/11003/members/14008
```

##### Response
The following is an example of the response. 
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.educationClass"
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create educationClass",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
