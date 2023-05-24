---
title: "wipeManagedAppRegistrationsByAzureAdDeviceId action"
description: "Issues a wipe operation on an app registration with specified aad device Id."
author: "jaiprakashmb"
localization_priority: Normal
ms.prod: "intune"
doc_type: apiPageType
---

# wipeManagedAppRegistrationsByAzureAdDeviceId action

Namespace: microsoft.graph

> **Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.

> **Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.

Issues a wipe operation on an app registration with specified aad device Id.

## Permissions
Choose the permission or permissions marked as least privileged for this API. Use a higher privileged permission or permissions [only if your app requires it](/graph/permissions-overview#best-practices-for-using-microsoft-graph-permissions). For details about delegated and application permissions, see [Permission types](/graph/permissions-overview#permission-types). To learn more about these permissions, see the [permissions reference](/graph/permissions-reference).

<!-- { "blockType": "permissions", "name": "intune_mam_user_wipemanagedappregistrationsbyazureaddeviceid" } -->
[!INCLUDE [permissions-table](../includes/permissions/intune-mam-user-wipemanagedappregistrationsbyazureaddeviceid-permissions.md)]

## HTTP Request
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /users/{usersId}/wipeManagedAppRegistrationsByAzureAdDeviceId
```

## Request headers
|Header|Value|
|:---|:---|
|Authorization|Bearer &lt;token&gt; Required.|
|Accept|application/json|

## Request body
In the request body, supply JSON representation of the parameters.

The following table shows the parameters that can be used with this action.

|Property|Type|Description|
|:---|:---|:---|
|azureAdDeviceId|String|Azure AD Device Id|



## Response
If successful, this action returns a `204 No Content` response code.

## Example

### Request
Here is an example of the request.
``` http
POST https://graph.microsoft.com/beta/users/{usersId}/wipeManagedAppRegistrationsByAzureAdDeviceId

Content-type: application/json
Content-length: 53

{
  "azureAdDeviceId": "Azure Ad Device Id value"
}
```

### Response
Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.
``` http
HTTP/1.1 204 No Content
```
