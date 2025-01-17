---
title: "Get backupRestoreRoot"
description: "Get the service status of the Microsoft 365 Backup Storage service in a tenant."
author: "tushar20"
ms.reviewer: "manikantsinghms"
ms.localizationpriority: medium
ms.subservice: "m365-backup-storage"
doc_type: apiPageType
---

# Get backupRestoreRoot

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Get the [serviceStatus](../resources/servicestatus.md) of the [Microsoft 365 Backup Storage](../resources/backuprestoreroot.md) service in a tenant.

[!INCLUDE [national-cloud-support](../../includes/global-only.md)]

## Permissions

Choose the permission or permissions marked as least privileged for this API. Use a higher privileged permission or permissions [only if your app requires it](/graph/permissions-overview#best-practices-for-using-microsoft-graph-permissions). For details about delegated and application permissions, see [Permission types](/graph/permissions-overview#permission-types). To learn more about these permissions, see the [permissions reference](/graph/permissions-reference).

<!-- { "blockType": "permissions", "name": "backuprestoreroot_get" } -->
[!INCLUDE [permissions-table](../includes/permissions/backuprestoreroot-get-permissions.md)]

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /solutions/backupRestore
```

## Request headers

|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required. Learn more about [authentication and authorization](/graph/auth/auth-concepts).|

## Request body

Don't supply a request body for this method.

## Response

If successful, this method returns a `200 OK` response code and a [backupRestoreRoot](../resources/backuprestoreroot.md) object in the response body.

## Examples

### Request

The following example shows a request.
<!-- {
  "blockType": "request",
  "name": "backuprestoreroot_get"
}
-->
``` http
GET https://graph.microsoft.com/beta/solutions/backupRestore
```


### Response

The following example shows the response.
>**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.backupRestoreRoot"
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "@odata.context": "https://graph.microsoft.com/beta/$metadata#solutions/backupRestore/$entity",
  "serviceStatus": {
      "status": "enabled",
      "disableReason": "none",
      "backupServiceConsumer": "firstparty",
      "lastModifiedDateTime": "2024-05-21T04:47:52.5769075Z",
      "lastModifiedBy": {
          "user": {
              "identity": "40927a5d-4f18-4966-9bfe-2e00cd1d0ee8"
          }
      }
  }
}
```

