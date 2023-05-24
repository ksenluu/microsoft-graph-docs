---
title: "Update deviceManagement"
description: "Update the properties of a deviceManagement object."
author: "dougeby"
ms.localizationpriority: medium
ms.prod: "intune"
doc_type: apiPageType
---

# Update deviceManagement

Namespace: microsoft.graph

> **Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.

Update the properties of a [deviceManagement](../resources/intune-troubleshooting-devicemanagement.md) object.

## Prerequisites
Choose the permission or permissions marked as least privileged for this API. Use a higher privileged permission or permissions [only if your app requires it](/graph/permissions-overview#best-practices-for-using-microsoft-graph-permissions). For details about delegated and application permissions, see [Permission types](/graph/permissions-overview#permission-types). To learn more about these permissions, see the [permissions reference](/graph/permissions-reference).

<!-- { "blockType": "permissions", "name": "intune_troubleshooting_devicemanagement_update" } -->
[!INCLUDE [permissions-table](../includes/permissions/intune-troubleshooting-devicemanagement-update-permissions.md)]

## HTTP Request
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement
```

## Request headers
|Header|Value|
|:---|:---|
|Authorization|Bearer &lt;token&gt; Required.|
|Accept|application/json|

## Request body
In the request body, supply a JSON representation for the [deviceManagement](../resources/intune-troubleshooting-devicemanagement.md) object.

The following table shows the properties that are required when you create the [deviceManagement](../resources/intune-troubleshooting-devicemanagement.md).

|Property|Type|Description|
|:---|:---|:---|
|id|String|Not yet documented|



## Response
If successful, this method returns a `200 OK` response code and an updated [deviceManagement](../resources/intune-troubleshooting-devicemanagement.md) object in the response body.

## Example

### Request
Here is an example of the request.
``` http
PATCH https://graph.microsoft.com/v1/deviceManagement
Content-type: application/json
Content-length: 58

{
  "@odata.type": "#microsoft.graph.deviceManagement"
}
```

### Response
Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 107

{
  "@odata.type": "#microsoft.graph.deviceManagement",
  "id": "0b283420-3420-0b28-2034-280b2034280b"
}
```




