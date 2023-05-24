---
title: "Get requestRemoteHelpSessionAccessResponse"
description: "Read properties and relationships of the requestRemoteHelpSessionAccessResponse object."
author: "jaiprakashmb"
localization_priority: Normal
ms.prod: "intune"
doc_type: apiPageType
---

# Get requestRemoteHelpSessionAccessResponse

Namespace: microsoft.graph

> **Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.

> **Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.

Read properties and relationships of the [requestRemoteHelpSessionAccessResponse](../resources/intune-remoteassistance-requestremotehelpsessionaccessresponse.md) object.

## Permissions
Choose the permission or permissions marked as least privileged for this API. Use a higher privileged permission or permissions [only if your app requires it](/graph/permissions-overview#best-practices-for-using-microsoft-graph-permissions). For details about delegated and application permissions, see [Permission types](/graph/permissions-overview#permission-types). To learn more about these permissions, see the [permissions reference](/graph/permissions-reference).

<!-- { "blockType": "permissions", "name": "intune_remoteassistance_requestremotehelpsessionaccessresponse_get" } -->
[!INCLUDE [permissions-table](../includes/permissions/intune-remoteassistance-requestremotehelpsessionaccessresponse-get-permissions.md)]

## HTTP Request
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /RequestRemoteHelpSessionAccessResponse/{RequestRemoteHelpSessionAccessResponseId}
```

## Optional query parameters
This method supports the [OData Query Parameters](/graph/query-parameters) to help customize the response.

## Request headers
|Header|Value|
|:---|:---|
|Authorization|Bearer &lt;token&gt; Required.|
|Accept|application/json|

## Request body
Do not supply a request body for this method.

## Response
If successful, this method returns a `200 OK` response code and [requestRemoteHelpSessionAccessResponse](../resources/intune-remoteassistance-requestremotehelpsessionaccessresponse.md) object in the response body.

## Example

### Request
Here is an example of the request.
``` http
GET https://graph.microsoft.com/beta/RequestRemoteHelpSessionAccessResponse/{RequestRemoteHelpSessionAccessResponseId}
```

### Response
Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 293

{
  "value": {
    "@odata.type": "#microsoft.graph.requestRemoteHelpSessionAccessResponse",
    "sessionKey": "Session Key value",
    "sessionType": "takeFullControl",
    "pubSubEncryptionKey": "Pub Sub Encryption Key value",
    "pubSubEncryption": "Pub Sub Encryption value"
  }
}
```
