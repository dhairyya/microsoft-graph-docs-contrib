---
title: "Get restoreSessionBase"
description: "Get the properties of restoreSessionBase by ID."
author: "tushar20"
ms.reviewer: "manikantsinghms"
ms.localizationpriority: medium
ms.subservice: "m365-backup-storage"
doc_type: apiPageType
---

# Get restoreSessionBase

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Get the properties of a [restoreSession](../resources/restoresessionbase.md) object by ID.

[!INCLUDE [national-cloud-support](../../includes/global-only.md)]

## Permissions

Choose the permission or permissions marked as least privileged for this API. Use a higher privileged permission or permissions [only if your app requires it](/graph/permissions-overview#best-practices-for-using-microsoft-graph-permissions). For details about delegated and application permissions, see [Permission types](/graph/permissions-overview#permission-types). To learn more about these permissions, see the [permissions reference](/graph/permissions-reference).

<!-- { "blockType": "permissions", "name": "restoresessionbase_get" } -->
[!INCLUDE [permissions-table](../includes/permissions/restoresessionbase-get-permissions.md)]

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /solutions/backupRestore/restoreSessions/{restoreSessionBaseId}
```

## Request headers

|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required. Learn more about [authentication and authorization](/graph/auth/auth-concepts).|

## Request body

Don't supply a request body for this method.

## Response

If successful, this method returns a `200 OK` response code and a [restoreSessionBase](../resources/restoresessionbase.md) object in the response body.

## Examples

### Request

The following example shows a request.
<!-- {
  "blockType": "request",
  "name": "restoresessionbase_get"
}
-->
``` http
GET https://graph.microsoft.com/beta/solutions/backupRestore/restoreSessions/959ba739-70b5-43c4-8c90-b2c22014f18b
```

### Response

The following example shows the response.
>**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.restoreSessionBase"
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "@odata.type": "#microsoft.graph.sharepointRestoreSession",
  "id": "959ba739-70b5-43c4-8c90-b2c22014f18b",
  "status": "active",
  "createdBy": {
    "application": {
      "id": "1fec8e78-bce4-4aaf-ab1b-5451cc387264",
      "displayName": "Microsoft Enhanced Restore"
    },
    "user": {
      "id": "845457dc-4bb2-4815-bef3-8628ebd1952e",
      "displayName": "Ryan"
    }
  },
  "createdDateTime": "2023-03-30T12-01-03.45Z",
  "lastModifiedBy": {
    "application": {
      "id": "1fec8e78-bce4-4aaf-ab1b-5451cc387264",
      "displayName": "Microsoft Enhanced Restore"
    },
    "user": {
      "id": "845457dc-4bb2-4815-bef3-8628ebd1952e",
      "displayName": "Ryan"
    }
  },
  "lastModifiedDateTime": "2023-03-30T12-01-03.45Z"
}
```
