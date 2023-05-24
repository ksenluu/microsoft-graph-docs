---
title: "Create microsoftTunnelServerLogCollectionResponse"
description: "Create a new microsoftTunnelServerLogCollectionResponse object."
author: "jaiprakashmb"
localization_priority: Normal
ms.prod: "intune"
doc_type: apiPageType
---

# Create microsoftTunnelServerLogCollectionResponse

Namespace: microsoft.graph

> **Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.

Create a new [microsoftTunnelServerLogCollectionResponse](../resources/intune-mstunnel-microsofttunnelserverlogcollectionresponse.md) object.

## Permissions
Choose the permission or permissions marked as least privileged for this API. Use a higher privileged permission or permissions [only if your app requires it](/graph/permissions-overview#best-practices-for-using-microsoft-graph-permissions). For details about delegated and application permissions, see [Permission types](/graph/permissions-overview#permission-types). To learn more about these permissions, see the [permissions reference](/graph/permissions-reference).

<!-- { "blockType": "permissions", "name": "intune_mstunnel_microsofttunnelserverlogcollectionresponse_create" } -->
[!INCLUDE [permissions-table](../includes/permissions/intune-mstunnel-microsofttunnelserverlogcollectionresponse-create-permissions.md)]

## HTTP Request
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/microsoftTunnelServerLogCollectionResponses
```

## Request headers
|Header|Value|
|:---|:---|
|Authorization|Bearer &lt;token&gt; Required.|
|Accept|application/json|

## Request body
In the request body, supply a JSON representation for the microsoftTunnelServerLogCollectionResponse object.

The following table shows the properties that are required when you create the microsoftTunnelServerLogCollectionResponse.

|Property|Type|Description|
|:---|:---|:---|
|id|String|The unique identifier for server log collection response. Read-only.|
|status|[microsoftTunnelLogCollectionStatus](../resources/intune-mstunnel-microsofttunnellogcollectionstatus.md)|The status of log collection. Possible values are: pending, completed, failed. Possible values are: `pending`, `completed`, `failed`, `unknownFutureValue`.|
|startDateTime|DateTimeOffset|The start time of the logs collected|
|endDateTime|DateTimeOffset|The end time of the logs collected|
|sizeInBytes|Int64|The size of the logs in bytes|
|serverId|String|ID of the server the log collection is requested upon|
|requestDateTime|DateTimeOffset|The time when the log collection was requested|
|expiryDateTime|DateTimeOffset|The time when the log collection is expired|



## Response
If successful, this method returns a `201 Created` response code and a [microsoftTunnelServerLogCollectionResponse](../resources/intune-mstunnel-microsofttunnelserverlogcollectionresponse.md) object in the response body.

## Example

### Request
Here is an example of the request.
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/microsoftTunnelServerLogCollectionResponses
Content-type: application/json
Content-length: 395

{
  "@odata.type": "#microsoft.graph.microsoftTunnelServerLogCollectionResponse",
  "status": "completed",
  "startDateTime": "2016-12-31T23:58:46.7156189-08:00",
  "endDateTime": "2017-01-01T00:03:30.9241974-08:00",
  "sizeInBytes": 11,
  "serverId": "Server Id value",
  "requestDateTime": "2017-01-01T00:03:07.1589002-08:00",
  "expiryDateTime": "2017-01-01T00:03:32.5199332-08:00"
}
```

### Response
Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 444

{
  "@odata.type": "#microsoft.graph.microsoftTunnelServerLogCollectionResponse",
  "id": "05dcc2e9-c2e9-05dc-e9c2-dc05e9c2dc05",
  "status": "completed",
  "startDateTime": "2016-12-31T23:58:46.7156189-08:00",
  "endDateTime": "2017-01-01T00:03:30.9241974-08:00",
  "sizeInBytes": 11,
  "serverId": "Server Id value",
  "requestDateTime": "2017-01-01T00:03:07.1589002-08:00",
  "expiryDateTime": "2017-01-01T00:03:32.5199332-08:00"
}
```
