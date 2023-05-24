---
title: "getDevicesScheduledToRetire function"
description: "Not yet documented"
author: "jaiprakashmb"
localization_priority: Normal
ms.prod: "intune"
doc_type: apiPageType
---

# getDevicesScheduledToRetire function

Namespace: microsoft.graph

> **Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.

> **Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.

Not yet documented

## Permissions
Choose the permission or permissions marked as least privileged for this API. Use a higher privileged permission or permissions [only if your app requires it](/graph/permissions-overview#best-practices-for-using-microsoft-graph-permissions). For details about delegated and application permissions, see [Permission types](/graph/permissions-overview#permission-types). To learn more about these permissions, see the [permissions reference](/graph/permissions-reference).

<!-- { "blockType": "permissions", "name": "intune_deviceconfig_devicecompliancepolicy_getdevicesscheduledtoretire" } -->
[!INCLUDE [permissions-table](../includes/permissions/intune-deviceconfig-devicecompliancepolicy-getdevicesscheduledtoretire-permissions.md)]

## HTTP Request
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceCompliancePolicies/getDevicesScheduledToRetire
```

## Request headers
|Header|Value|
|:---|:---|
|Authorization|Bearer &lt;token&gt; Required.|
|Accept|application/json|

## Request body
Do not supply a request body for this method.

## Response
If successful, this function returns a `200 OK` response code and a [retireScheduledManagedDevice](../resources/intune-deviceconfig-retirescheduledmanageddevice.md) collection in the response body.

## Example

### Request
Here is an example of the request.
``` http
GET https://graph.microsoft.com/beta/deviceManagement/deviceCompliancePolicies/getDevicesScheduledToRetire
```

### Response
Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 670

{
  "value": [
    {
      "@odata.type": "microsoft.graph.retireScheduledManagedDevice",
      "id": "Id value",
      "managedDeviceId": "Managed Device Id value",
      "managedDeviceName": "Managed Device Name value",
      "deviceType": "windowsRT",
      "complianceState": "notApplicable",
      "retireAfterDateTime": "2016-12-31T23:57:37.576134-08:00",
      "managementAgent": "mdm",
      "ownerType": "company",
      "deviceCompliancePolicyName": "Device Compliance Policy Name value",
      "deviceCompliancePolicyId": "Device Compliance Policy Id value",
      "roleScopeTagIds": [
        "Role Scope Tag Ids value"
      ]
    }
  ]
}
```
