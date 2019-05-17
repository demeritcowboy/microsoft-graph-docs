---
author: rgregg
ms.author: rgregg
description: Create a copy of an existing item.
title: check-out a driveItem resource
ms.prod: "sharepoint"
---
# check-out a driveItem resource

Check-out a driveItem resource to prevent others from editing the document, and your changes from being visible until the documented is [checked-in](driveitem_checkin.md).

## Permissions

One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

|Permission type      | Permissions (from least to most privileged)              |
|:--------------------|:---------------------------------------------------------|
|Delegated (work or school account) | Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All    |
|Delegated (personal Microsoft account) | Files.ReadWrite, Files.ReadWrite.All    |
|Application | Files.ReadWrite.All, Sites.ReadWrite.All |

## HTTP request

<!-- { "blockType": "ignored" } -->

```http
POST /drives/{driveId}/items/{itemId}/checkout
POST /groups/{groupId}/drive/items/{itemId}/checkout
POST /me/drive/items/{item-id}/checkout
POST /sites/{siteId}/drive/items/{itemId}/checkout
POST /users/{userId}/drive/items/{itemId}/checkout
```

### Request body

No request body is required.

## Response

If successful, the API call returns a `204 No Content`.

## Example

### Request

This example checks out a file identified by `{item-id}`.

<!-- { "blockType": "request", "name": "checkout-item", "scopes": "files.readwrite sites.readwrite.all", "target": "action", "apiVersions": "beta" } -->

```http
POST /drives/{drive-id}/items/{item-id}/checkout
```

### Response

<!-- { "blockType": "response" } -->

```http
HTTP/1.1 204 No Content
```


[item-resource]: ../resources/driveitem.md

<!-- {
  "type": "#page.annotation",
  "description": "Create a copy of an existing item.",
  "keywords": "copy existing item",
  "section": "documentation",
  "tocPath": "Items/Copy"
} -->