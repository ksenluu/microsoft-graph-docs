---
title: "Create createRemoteHelpSessionResponse"
description: "Create a new createRemoteHelpSessionResponse object."
author: "jaiprakashmb"
localization_priority: Normal
ms.prod: "intune"
doc_type: apiPageType
---

# Create createRemoteHelpSessionResponse

Namespace: microsoft.graph

> **Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.

> **Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.

Create a new [createRemoteHelpSessionResponse](../resources/intune-remoteassistance-createremotehelpsessionresponse.md) object.

## Permissions
Choose the permission or permissions marked as least privileged for this API. Use a higher privileged permission or permissions [only if your app requires it](/graph/permissions-overview#best-practices-for-using-microsoft-graph-permissions). For details about delegated and application permissions, see [Permission types](/graph/permissions-overview#permission-types). To learn more about these permissions, see the [permissions reference](/graph/permissions-reference).

<!-- { "blockType": "permissions", "name": "intune_remoteassistance_createremotehelpsessionresponse_create" } -->
[!INCLUDE [permissions-table](../includes/permissions/intune-remoteassistance-createremotehelpsessionresponse-create-permissions.md)]

## HTTP Request
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /CreateRemoteHelpSessionResponse
```

## Request headers
|Header|Value|
|:---|:---|
|Authorization|Bearer &lt;token&gt; Required.|
|Accept|application/json|

## Request body
In the request body, supply a JSON representation for the createRemoteHelpSessionResponse object.

The following table shows the properties that are required when you create the createRemoteHelpSessionResponse.

|Property|Type|Description|
|:---|:---|:---|
|sessionKey|String|The unique identifier for a session|
|sessionType|[allowedRemoteAssistanceActions](../resources/intune-remoteassistance-allowedremoteassistanceactions.md)|Remote Help Session Type. Possible values are: `viewScreen`, `takeFullControl`, `elevation`, `unattended`, `unknownFutureValue`.|



## Response
If successful, this method returns a `201 Created` response code and a [createRemoteHelpSessionResponse](../resources/intune-remoteassistance-createremotehelpsessionresponse.md) object in the response body.

## Example

### Request
Here is an example of the request.
``` http
POST https://graph.microsoft.com/beta/CreateRemoteHelpSessionResponse
Content-type: application/json
Content-length: 148

{
  "@odata.type": "#microsoft.graph.createRemoteHelpSessionResponse",
  "sessionKey": "Session Key value",
  "sessionType": "takeFullControl"
}
```

### Response
Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 148

{
  "@odata.type": "#microsoft.graph.createRemoteHelpSessionResponse",
  "sessionKey": "Session Key value",
  "sessionType": "takeFullControl"
}
```
