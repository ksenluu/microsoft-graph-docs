---
title: "List windowsManagedAppProtections"
description: "List properties and relationships of the windowsManagedAppProtection objects."
author: "jaiprakashmb"
localization_priority: Normal
ms.prod: "intune"
doc_type: apiPageType
---

# List windowsManagedAppProtections

Namespace: microsoft.graph

> **Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.

> **Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.

List properties and relationships of the [windowsManagedAppProtection](../resources/intune-mam-windowsmanagedappprotection.md) objects.

## Permissions
Choose the permission or permissions marked as least privileged for this API. Use a higher privileged permission or permissions [only if your app requires it](/graph/permissions-overview#best-practices-for-using-microsoft-graph-permissions). For details about delegated and application permissions, see [Permission types](/graph/permissions-overview#permission-types). To learn more about these permissions, see the [permissions reference](/graph/permissions-reference).

<!-- { "blockType": "permissions", "name": "intune_mam_windowsmanagedappprotection_list" } -->
[!INCLUDE [permissions-table](../includes/permissions/intune-mam-windowsmanagedappprotection-list-permissions.md)]

## HTTP Request
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/windowsManagedAppProtections
```

## Request headers
|Header|Value|
|:---|:---|
|Authorization|Bearer &lt;token&gt; Required.|
|Accept|application/json|

## Request body
Do not supply a request body for this method.

## Response
If successful, this method returns a `200 OK` response code and a collection of [windowsManagedAppProtection](../resources/intune-mam-windowsmanagedappprotection.md) objects in the response body.

## Example

### Request
Here is an example of the request.
``` http
GET https://graph.microsoft.com/beta/deviceAppManagement/windowsManagedAppProtections
```

### Response
Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1786

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.windowsManagedAppProtection",
      "displayName": "Display Name value",
      "description": "Description value",
      "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
      "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
      "roleScopeTagIds": [
        "Role Scope Tag Ids value"
      ],
      "id": "c7894cd1-4cd1-c789-d14c-89c7d14c89c7",
      "version": "Version value",
      "isAssigned": true,
      "deployedAppCount": 0,
      "printBlocked": true,
      "allowedInboundDataTransferSources": "none",
      "allowedOutboundClipboardSharingLevel": "none",
      "allowedOutboundDataTransferDestinations": "none",
      "appActionIfUnableToAuthenticateUser": "wipe",
      "maximumAllowedDeviceThreatLevel": "secured",
      "mobileThreatDefenseRemediationAction": "wipe",
      "minimumRequiredSdkVersion": "Minimum Required Sdk Version value",
      "minimumWipeSdkVersion": "Minimum Wipe Sdk Version value",
      "minimumRequiredOsVersion": "Minimum Required Os Version value",
      "minimumWarningOsVersion": "Minimum Warning Os Version value",
      "minimumWipeOsVersion": "Minimum Wipe Os Version value",
      "minimumRequiredAppVersion": "Minimum Required App Version value",
      "minimumWarningAppVersion": "Minimum Warning App Version value",
      "minimumWipeAppVersion": "Minimum Wipe App Version value",
      "maximumRequiredOsVersion": "Maximum Required Os Version value",
      "maximumWarningOsVersion": "Maximum Warning Os Version value",
      "maximumWipeOsVersion": "Maximum Wipe Os Version value",
      "periodOfflineBeforeWipeIsEnforced": "-PT3M22.1587532S",
      "periodOfflineBeforeAccessCheck": "-PT17.1357909S"
    }
  ]
}
```
