---
title: "protectionRuleBase: run"
description: "Activate a protection rule associated with a protection policy."
author: "tushar20"
ms.reviewer: "manikantsinghms"
ms.localizationpriority: medium
ms.subservice: "m365-backup-storage"
doc_type: apiPageType
---

# protectionRuleBase: run

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Activate a [protection rule](../resources/protectionrulebase.md).

Upon activating the protection rule, the status transitions to `active`.

## Permissions

Choose the permission or permissions marked as least privileged for this API. Use a higher privileged permission or permissions [only if your app requires it](/graph/permissions-overview#best-practices-for-using-microsoft-graph-permissions). For details about delegated and application permissions, see [Permission types](/graph/permissions-overview#permission-types). To learn more about these permissions, see the [permissions reference](/graph/permissions-reference).

<!-- { "blockType": "permissions", "name": "protectionrulebase_run" } -->
[!INCLUDE [permissions-table](../includes/permissions/protectionrulebase-run-permissions.md)]

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /solutions/backupRestore/sharePointProtectionPolicies/{sharePointProtectionPolicyId}/siteInclusionRules/{siteProtectionRuleId}/run
POST /solutions/backupRestore/oneDriveForBusinessProtectionPolicies/{oneDriveForBusinessProtectionPolicyId}/driveInclusionRules/{driveProtectionRuleId}/run
POST /solutions/backupRestore/exchangeProtectionPolicies/{exchangeProtectionPolicyId}/mailboxInclusionRules/{mailboxProtectionRuleId}/run
```

## Request headers

|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required. Learn more about [authentication and authorization](/graph/auth/auth-concepts).|

## Request body

Don't supply a request body for this method.

## Response

If successful, this action returns a `200 OK` response code and a [protectionRuleBase](../resources/protectionrulebase.md) object in the response body.

## Examples

### Example 1: Activate a siteInclusionRule associated with a SharePoint protection policy

The following example shows how to activate a **siteInclusionRule** associated with a [sharePointProtectionPolicy](../resources/sharepointprotectionpolicy.md) object.

#### Request

The following example shows a request.
<!-- {
  "blockType": "request",
  "name": "siteprotectionrulethis.run"
}
-->
``` http
POST https://graph.microsoft.com/beta/solutions/backupRestore/sharePointProtectionPolicies/71633878-8321-4950-bfaf-ed285bdd1461/siteInclusionRules/61633878-8321-4950-bfaf-ed285bdd1461/run
```

#### Response

The following example shows the response.
>**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.protectionRuleBase"
}
-->
``` http
HTTP/1.1 202 Accepted
Content-Type: application/json
Content-Location: https://graph.microsoft.com/beta/solutions/backupRestore/sharePointProtectionPolicies/71633878-8321-4950-bfaf-ed285bdd1461/siteInclusionRules('61633878-8321-4950-bfaf-ed285bdd1461')

{
   "@odata.type": "#microsoft.graph.protectionRuleBase",
   "id":"61633878-8321-4950-bfaf-ed285bdd1461",
   "status" : "active",
   "createdBy":{
      "application":{
         "id":"1fec8e78-bce4-4aaf-ab1b-5451cc387264"
      },
      "user":{
         "id":"845457dc-4bb2-4815-bef3-8628ebd1952e"
      }
   },
   "createdDateTime":"2015-06-19T12-01-03.45Z",
   "lastModifiedBy":{
      "application":{
         "id":"1fec8e78-bce4-4aaf-ab1b-5451cc387264"
      },
      "user":{
         "id":"845457dc-4bb2-4815-bef3-8628ebd1952e"
      }
   },
   "lastModifiedDateTime":"2015-06-19T12-01-03.45Z",
   "isAutoApplyEnabled": false
}
```

### Example 2: Activate a driveInclusionRule associated with an OneDriveForBusiness protection policy

The following example shows how to activate a **driveInclusionRule**associated with an [oneDriveForBusinessProtectionPolicy](../resources/onedriveforbusinessprotectionpolicy.md) object.

### Request

The following example shows a request.
<!-- {
  "blockType": "request",
  "name": "driveprotectionrulethis_run"
}
-->
``` http
POST https://graph.microsoft.com/beta/solutions/backupRestore/oneDriveForBusinessProtectionPolicies/71633878-8321-4950-bfaf-ed285bdd1461/driveInclusionRules/61633878-8321-4950-bfaf-ed285bdd1461/run
```

### Response

The following example shows the response.
>**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.protectionRuleBase"
}
-->
``` http
HTTP/1.1 202 Accepted
Content-Type: application/json
Content-Location: https://graph.microsoft.com/beta/solutions/backupRestore/oneDriveForBusinessProtectionPolicies/71633878-8321-4950-bfaf-ed285bdd1461/driveInclusionRules('61633878-8321-4950-bfaf-ed285bdd1461')

{
   "@odata.type": "#microsoft.graph.protectionRuleBase",
   "id":"61633878-8321-4950-bfaf-ed285bdd1461",
   "status" : "active",
   "createdBy":{
      "application":{
         "id":"1fec8e78-bce4-4aaf-ab1b-5451cc387264"
      },
      "user":{
         "id":"845457dc-4bb2-4815-bef3-8628ebd1952e"
      }
   },
   "createdDateTime":"2015-06-19T12-01-03.45Z",
   "lastModifiedBy":{
      "application":{
         "id":"1fec8e78-bce4-4aaf-ab1b-5451cc387264"
      },
      "user":{
         "id":"845457dc-4bb2-4815-bef3-8628ebd1952e"
      }
   },
   "lastModifiedDateTime":"2015-06-19T12-01-03.45Z",
   "isAutoApplyEnabled": false
}
```

### Example 3: Activate a mailboxInclusionRule associated with an Exchange protection policy

The following example shows how to activate a **mailboxInclusionRule** associated with an [exchangeProtectionPolicy](../resources/exchangeprotectionpolicy.md) object.

#### Request

The following example shows a request.
<!-- {
  "blockType": "request",
  "name": "mailboxprotectionrulethis.run"
}
-->
``` http
POST https://graph.microsoft.com/beta/solutions/backupRestore/exchangeProtectionPolicies/{exchangeProtectionPolicyId}/mailboxInclusionRules/{mailboxProtectionRuleId}/run
```

#### Response

The following example shows the response.
>**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.protectionRuleBase"
}
-->
``` http
HTTP/1.1 202 Accepted
Content-Type: application/json
Content-Location: https://graph.microsoft.com/beta/solutions/backupRestore/exchangeProtectionPolicies/{exchangeProtectionPolicyId}/mailboxInclusionRules/{mailboxProtectionRuleId}

{
   "@odata.type": "#microsoft.graph.protectionRuleBase",
   "id":"41633878-8321-4950-bfaf-ed285bdd1461",
   "status" : "active",
   "createdBy":{
      "application":{
         "id":"1fec8e78-bce4-4aaf-ab1b-5451cc387264"
      },
      "user":{
         "id":"845457dc-4bb2-4815-bef3-8628ebd1952e"
      }
   },
   "createdDateTime":"2015-06-19T12-01-03.45Z",
   "lastModifiedBy":{
      "application":{
         "id":"1fec8e78-bce4-4aaf-ab1b-5451cc387264"
      },
      "user":{
         "id":"845457dc-4bb2-4815-bef3-8628ebd1952e"
      }
   },
   "lastModifiedDateTime":"2015-06-19T12-01-03.45Z",
   "isAutoApplyEnabled": false
}
```
