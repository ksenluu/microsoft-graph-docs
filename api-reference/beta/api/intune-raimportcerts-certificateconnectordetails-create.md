---
title: "Create certificateConnectorDetails"
description: "Create a new certificateConnectorDetails object."
author: "jaiprakashmb"
localization_priority: Normal
ms.prod: "intune"
doc_type: apiPageType
---

# Create certificateConnectorDetails

Namespace: microsoft.graph

> **Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.

> **Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.

Create a new [certificateConnectorDetails](../resources/intune-raimportcerts-certificateconnectordetails.md) object.

## Permissions
Choose the permission or permissions marked as least privileged for this API. Use a higher privileged permission or permissions [only if your app requires it](/graph/permissions-overview#best-practices-for-using-microsoft-graph-permissions). For details about delegated and application permissions, see [Permission types](/graph/permissions-overview#permission-types). To learn more about these permissions, see the [permissions reference](/graph/permissions-reference).

<!-- { "blockType": "permissions", "name": "intune_raimportcerts_certificateconnectordetails_create" } -->
[!INCLUDE [permissions-table](../includes/permissions/intune-raimportcerts-certificateconnectordetails-create-permissions.md)]

## HTTP Request
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/certificateConnectorDetails
```

## Request headers
|Header|Value|
|:---|:---|
|Authorization|Bearer &lt;token&gt; Required.|
|Accept|application/json|

## Request body
In the request body, supply a JSON representation for the certificateConnectorDetails object.

The following table shows the properties that are required when you create the certificateConnectorDetails.

|Property|Type|Description|
|:---|:---|:---|
|id|String|Unique identifier for this set of ConnectorDetails.|
|connectorName|String|Connector name (set during enrollment).|
|machineName|String|Name of the machine hosting this connector service.|
|enrollmentDateTime|DateTimeOffset|Date/time when this connector was enrolled.|
|lastCheckinDateTime|DateTimeOffset|Date/time when this connector last connected to the service.|
|connectorVersion|String|Version of the connector installed.|



## Response
If successful, this method returns a `201 Created` response code and a [certificateConnectorDetails](../resources/intune-raimportcerts-certificateconnectordetails.md) object in the response body.

## Example

### Request
Here is an example of the request.
``` http
POST https://graph.microsoft.com/beta/deviceManagement/certificateConnectorDetails
Content-type: application/json
Content-length: 328

{
  "@odata.type": "#microsoft.graph.certificateConnectorDetails",
  "connectorName": "Connector Name value",
  "machineName": "Machine Name value",
  "enrollmentDateTime": "2016-12-31T23:57:59.3726057-08:00",
  "lastCheckinDateTime": "2017-01-01T00:02:46.0431416-08:00",
  "connectorVersion": "Connector Version value"
}
```

### Response
Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 377

{
  "@odata.type": "#microsoft.graph.certificateConnectorDetails",
  "id": "104d7361-7361-104d-6173-4d1061734d10",
  "connectorName": "Connector Name value",
  "machineName": "Machine Name value",
  "enrollmentDateTime": "2016-12-31T23:57:59.3726057-08:00",
  "lastCheckinDateTime": "2017-01-01T00:02:46.0431416-08:00",
  "connectorVersion": "Connector Version value"
}
```
