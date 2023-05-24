---
title: "Update hardwarePasswordInfo"
description: "Update the properties of a hardwarePasswordInfo object."
author: "jaiprakashmb"
localization_priority: Normal
ms.prod: "intune"
doc_type: apiPageType
---

# Update hardwarePasswordInfo

Namespace: microsoft.graph

> **Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.

> **Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.

Update the properties of a [hardwarePasswordInfo](../resources/intune-deviceconfig-hardwarepasswordinfo.md) object.

## Permissions
Choose the permission or permissions marked as least privileged for this API. Use a higher privileged permission or permissions [only if your app requires it](/graph/permissions-overview#best-practices-for-using-microsoft-graph-permissions). For details about delegated and application permissions, see [Permission types](/graph/permissions-overview#permission-types). To learn more about these permissions, see the [permissions reference](/graph/permissions-reference).

<!-- { "blockType": "permissions", "name": "intune_deviceconfig_hardwarepasswordinfo_update" } -->
[!INCLUDE [permissions-table](../includes/permissions/intune-deviceconfig-hardwarepasswordinfo-update-permissions.md)]

## HTTP Request
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/hardwarePasswordInfo/{hardwarePasswordInfoId}
```

## Request headers
|Header|Value|
|:---|:---|
|Authorization|Bearer &lt;token&gt; Required.|
|Accept|application/json|

## Request body
In the request body, supply a JSON representation for the [hardwarePasswordInfo](../resources/intune-deviceconfig-hardwarepasswordinfo.md) object.

The following table shows the properties that are required when you create the [hardwarePasswordInfo](../resources/intune-deviceconfig-hardwarepasswordinfo.md).

|Property|Type|Description|
|:---|:---|:---|
|id|String|Unique Identifier for the hardware password info|
|serialNumber|String|Device serial number|
|currentPassword|String|Current device password|
|previousPasswords|String collection|List of previous device passwords|



## Response
If successful, this method returns a `200 OK` response code and an updated [hardwarePasswordInfo](../resources/intune-deviceconfig-hardwarepasswordinfo.md) object in the response body.

## Example

### Request
Here is an example of the request.
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/hardwarePasswordInfo/{hardwarePasswordInfoId}
Content-type: application/json
Content-length: 216

{
  "@odata.type": "#microsoft.graph.hardwarePasswordInfo",
  "serialNumber": "Serial Number value",
  "currentPassword": "Current Password value",
  "previousPasswords": [
    "Previous Passwords value"
  ]
}
```

### Response
Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 265

{
  "@odata.type": "#microsoft.graph.hardwarePasswordInfo",
  "id": "418e4bb4-4bb4-418e-b44b-8e41b44b8e41",
  "serialNumber": "Serial Number value",
  "currentPassword": "Current Password value",
  "previousPasswords": [
    "Previous Passwords value"
  ]
}
```
