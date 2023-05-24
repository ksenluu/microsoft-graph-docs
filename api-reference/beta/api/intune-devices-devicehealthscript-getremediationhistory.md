---
title: "getRemediationHistory function"
description: "Function to get the number of remediations by a device health scripts"
author: "jaiprakashmb"
localization_priority: Normal
ms.prod: "intune"
doc_type: apiPageType
---

# getRemediationHistory function

Namespace: microsoft.graph

> **Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.

> **Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.

Function to get the number of remediations by a device health scripts

## Permissions
Choose the permission or permissions marked as least privileged for this API. Use a higher privileged permission or permissions [only if your app requires it](/graph/permissions-overview#best-practices-for-using-microsoft-graph-permissions). For details about delegated and application permissions, see [Permission types](/graph/permissions-overview#permission-types). To learn more about these permissions, see the [permissions reference](/graph/permissions-reference).

<!-- { "blockType": "permissions", "name": "intune_devices_devicehealthscript_getremediationhistory" } -->
[!INCLUDE [permissions-table](../includes/permissions/intune-devices-devicehealthscript-getremediationhistory-permissions.md)]

## HTTP Request
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceHealthScripts/{deviceHealthScriptId}/getRemediationHistory
```

## Request headers
|Header|Value|
|:---|:---|
|Authorization|Bearer &lt;token&gt; Required.|
|Accept|application/json|

## Request body
Do not supply a request body for this method.

## Response
If successful, this function returns a `200 OK` response code and a [deviceHealthScriptRemediationHistory](../resources/intune-devices-devicehealthscriptremediationhistory.md) in the response body.

## Example

### Request
Here is an example of the request.
``` http
GET https://graph.microsoft.com/beta/deviceManagement/deviceHealthScripts/{deviceHealthScriptId}/getRemediationHistory
```

### Response
Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 397

{
  "value": {
    "@odata.type": "microsoft.graph.deviceHealthScriptRemediationHistory",
    "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
    "historyData": [
      {
        "@odata.type": "microsoft.graph.deviceHealthScriptRemediationHistoryData",
        "date": "2016-12-31",
        "remediatedDeviceCount": 5,
        "noIssueDeviceCount": 2
      }
    ]
  }
}
```
