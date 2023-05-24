---
title: "List retrieveRemoteHelpSessionResponses"
description: "List properties and relationships of the retrieveRemoteHelpSessionResponse objects."
author: "jaiprakashmb"
localization_priority: Normal
ms.prod: "intune"
doc_type: apiPageType
---

# List retrieveRemoteHelpSessionResponses

Namespace: microsoft.graph

> **Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.

> **Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.

List properties and relationships of the [retrieveRemoteHelpSessionResponse](../resources/intune-remoteassistance-retrieveremotehelpsessionresponse.md) objects.

## Permissions
Choose the permission or permissions marked as least privileged for this API. Use a higher privileged permission or permissions [only if your app requires it](/graph/permissions-overview#best-practices-for-using-microsoft-graph-permissions). For details about delegated and application permissions, see [Permission types](/graph/permissions-overview#permission-types). To learn more about these permissions, see the [permissions reference](/graph/permissions-reference).

<!-- { "blockType": "permissions", "name": "intune_remoteassistance_retrieveremotehelpsessionresponse_list" } -->
[!INCLUDE [permissions-table](../includes/permissions/intune-remoteassistance-retrieveremotehelpsessionresponse-list-permissions.md)]

## HTTP Request
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /RemoteHelpSessionRetrieveResponse
```

## Request headers
|Header|Value|
|:---|:---|
|Authorization|Bearer &lt;token&gt; Required.|
|Accept|application/json|

## Request body
Do not supply a request body for this method.

## Response
If successful, this method returns a `200 OK` response code and a collection of [retrieveRemoteHelpSessionResponse](../resources/intune-remoteassistance-retrieveremotehelpsessionresponse.md) objects in the response body.

## Example

### Request
Here is an example of the request.
``` http
GET https://graph.microsoft.com/beta/RemoteHelpSessionRetrieveResponse
```

### Response
Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 638

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.retrieveRemoteHelpSessionResponse",
      "sessionKey": "Session Key value",
      "acsHelperUserToken": "Acs Helper User Token value",
      "acsHelperUserId": "Acs Helper User Id value",
      "acsSharerUserId": "Acs Sharer User Id value",
      "acsGroupId": "Acs Group Id value",
      "sessionType": "takeFullControl",
      "deviceName": "Device Name value",
      "pubSubGroupId": "Pub Sub Group Id value",
      "pubSubHelperAccessUri": "Pub Sub Helper Access Uri value",
      "sessionExpirationDateTime": "2016-12-31T23:59:57.5564522-08:00"
    }
  ]
}
```
