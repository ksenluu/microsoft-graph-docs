---
title: "reportRemoteAssistance action"
description: "A post call to submit the reporting payload"
author: "jaiprakashmb"
localization_priority: Normal
ms.prod: "intune"
doc_type: apiPageType
---

# reportRemoteAssistance action

Namespace: microsoft.graph

> **Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.

> **Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.

A post call to submit the reporting payload

## Permissions
Choose the permission or permissions marked as least privileged for this API. Use a higher privileged permission or permissions [only if your app requires it](/graph/permissions-overview#best-practices-for-using-microsoft-graph-permissions). For details about delegated and application permissions, see [Permission types](/graph/permissions-overview#permission-types). To learn more about these permissions, see the [permissions reference](/graph/permissions-reference).

<!-- { "blockType": "permissions", "name": "intune_remoteassistance_devicemanagement_reportremoteassistance" } -->
[!INCLUDE [permissions-table](../includes/permissions/intune-remoteassistance-devicemanagement-reportremoteassistance-permissions.md)]

## HTTP Request
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/reportRemoteAssistance
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
|reportingPayload|[remoteAssistanceReporting](../resources/intune-remoteassistance-remoteassistancereporting.md)|Not yet documented|



## Response
If successful, this action returns a `204 No Content` response code.

## Example

### Request
Here is an example of the request.
``` http
POST https://graph.microsoft.com/beta/deviceManagement/reportRemoteAssistance

Content-type: application/json
Content-length: 1195

{
  "reportingPayload": {
    "@odata.type": "microsoft.graph.remoteAssistanceReporting",
    "id": "Id value",
    "startDateTime": "2016-12-31T23:58:46.7156189-08:00",
    "endDateTime": "2017-01-01T00:03:30.9241974-08:00",
    "remoteAssistanceSessionType": "fullControl",
    "helperEmail": "Helper Email value",
    "helperTenantId": "Helper Tenant Id value",
    "helperUserId": "Helper User Id value",
    "helperFirstName": "Helper First Name value",
    "helperLastName": "Helper Last Name value",
    "helperOs": "Helper Os value",
    "deviceId": "Device Id value",
    "helperDeviceAadId": "Helper Device Aad Id value",
    "helperDeviceName": "Helper Device Name value",
    "helperEnrollmentState": "enrolled",
    "sharerEmail": "Sharer Email value",
    "sharerTenantId": "Sharer Tenant Id value",
    "sharerFirstName": "Sharer First Name value",
    "sharerLastName": "Sharer Last Name value",
    "sharerDeviceAadId": "Sharer Device Aad Id value",
    "sharerDeviceName": "Sharer Device Name value",
    "sharerOs": "Sharer Os value",
    "sharerEnrollmentState": "enrolled",
    "sharerDeviceSerialNumber": "Sharer Device Serial Number value"
  }
}
```

### Response
Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.
``` http
HTTP/1.1 204 No Content
```
