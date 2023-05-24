---
title: "List userExperienceAnalyticsWorkFromAnywhereModelPerformances"
description: "List properties and relationships of the userExperienceAnalyticsWorkFromAnywhereModelPerformance objects."
author: "jaiprakashmb"
localization_priority: Normal
ms.prod: "intune"
doc_type: apiPageType
---

# List userExperienceAnalyticsWorkFromAnywhereModelPerformances

Namespace: microsoft.graph

> **Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.

> **Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.

List properties and relationships of the [userExperienceAnalyticsWorkFromAnywhereModelPerformance](../resources/intune-devices-userexperienceanalyticsworkfromanywheremodelperformance.md) objects.

## Permissions
Choose the permission or permissions marked as least privileged for this API. Use a higher privileged permission or permissions [only if your app requires it](/graph/permissions-overview#best-practices-for-using-microsoft-graph-permissions). For details about delegated and application permissions, see [Permission types](/graph/permissions-overview#permission-types). To learn more about these permissions, see the [permissions reference](/graph/permissions-reference).

<!-- { "blockType": "permissions", "name": "intune_devices_userexperienceanalyticsworkfromanywheremodelperformance_list" } -->
[!INCLUDE [permissions-table](../includes/permissions/intune-devices-userexperienceanalyticsworkfromanywheremodelperformance-list-permissions.md)]

## HTTP Request
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/userExperienceAnalyticsWorkFromAnywhereModelPerformance
```

## Request headers
|Header|Value|
|:---|:---|
|Authorization|Bearer &lt;token&gt; Required.|
|Accept|application/json|

## Request body
Do not supply a request body for this method.

## Response
If successful, this method returns a `200 OK` response code and a collection of [userExperienceAnalyticsWorkFromAnywhereModelPerformance](../resources/intune-devices-userexperienceanalyticsworkfromanywheremodelperformance.md) objects in the response body.

## Example

### Request
Here is an example of the request.
``` http
GET https://graph.microsoft.com/beta/deviceManagement/userExperienceAnalyticsWorkFromAnywhereModelPerformance
```

### Response
Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 537

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.userExperienceAnalyticsWorkFromAnywhereModelPerformance",
      "id": "7ec79407-9407-7ec7-0794-c77e0794c77e",
      "model": "Model value",
      "manufacturer": "Manufacturer value",
      "modelDeviceCount": 0,
      "workFromAnywhereScore": 7.0,
      "windowsScore": 4.0,
      "cloudManagementScore": 6.666666666666667,
      "cloudIdentityScore": 6.0,
      "cloudProvisioningScore": 7.333333333333333,
      "healthStatus": "insufficientData"
    }
  ]
}
```
