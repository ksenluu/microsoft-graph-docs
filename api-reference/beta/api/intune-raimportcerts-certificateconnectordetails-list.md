---
title: "List certificateConnectorDetailses"
description: "List properties and relationships of the certificateConnectorDetails objects."
author: "jaiprakashmb"
localization_priority: Normal
ms.prod: "intune"
doc_type: apiPageType
---

# List certificateConnectorDetailses

Namespace: microsoft.graph

> **Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.

> **Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.

List properties and relationships of the [certificateConnectorDetails](../resources/intune-raimportcerts-certificateconnectordetails.md) objects.

## Permissions
Choose the permission or permissions marked as least privileged for this API. Use a higher privileged permission or permissions [only if your app requires it](/graph/permissions-overview#best-practices-for-using-microsoft-graph-permissions). For details about delegated and application permissions, see [Permission types](/graph/permissions-overview#permission-types). To learn more about these permissions, see the [permissions reference](/graph/permissions-reference).

<!-- { "blockType": "permissions", "name": "intune_raimportcerts_certificateconnectordetails_list" } -->
[!INCLUDE [permissions-table](../includes/permissions/intune-raimportcerts-certificateconnectordetails-list-permissions.md)]

## HTTP Request
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/certificateConnectorDetails
```

## Request headers
|Header|Value|
|:---|:---|
|Authorization|Bearer &lt;token&gt; Required.|
|Accept|application/json|

## Request body
Do not supply a request body for this method.

## Response
If successful, this method returns a `200 OK` response code and a collection of [certificateConnectorDetails](../resources/intune-raimportcerts-certificateconnectordetails.md) objects in the response body.

## Example

### Request
Here is an example of the request.
``` http
GET https://graph.microsoft.com/beta/deviceManagement/certificateConnectorDetails
```

### Response
Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 438

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.certificateConnectorDetails",
      "id": "104d7361-7361-104d-6173-4d1061734d10",
      "connectorName": "Connector Name value",
      "machineName": "Machine Name value",
      "enrollmentDateTime": "2016-12-31T23:57:59.3726057-08:00",
      "lastCheckinDateTime": "2017-01-01T00:02:46.0431416-08:00",
      "connectorVersion": "Connector Version value"
    }
  ]
}
```
