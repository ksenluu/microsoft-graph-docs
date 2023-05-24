---
title: "Update extendRemoteHelpSessionResponse"
description: "Update the properties of a extendRemoteHelpSessionResponse object."
author: "jaiprakashmb"
localization_priority: Normal
ms.prod: "intune"
doc_type: apiPageType
---

# Update extendRemoteHelpSessionResponse

Namespace: microsoft.graph

> **Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.

> **Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.

Update the properties of a [extendRemoteHelpSessionResponse](../resources/intune-remoteassistance-extendremotehelpsessionresponse.md) object.

## Permissions
Choose the permission or permissions marked as least privileged for this API. Use a higher privileged permission or permissions [only if your app requires it](/graph/permissions-overview#best-practices-for-using-microsoft-graph-permissions). For details about delegated and application permissions, see [Permission types](/graph/permissions-overview#permission-types). To learn more about these permissions, see the [permissions reference](/graph/permissions-reference).

<!-- { "blockType": "permissions", "name": "intune_remoteassistance_extendremotehelpsessionresponse_update" } -->
[!INCLUDE [permissions-table](../includes/permissions/intune-remoteassistance-extendremotehelpsessionresponse-update-permissions.md)]

## HTTP Request
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /ExtendRemoteHelpSessionResponse/{ExtendRemoteHelpSessionResponseId}
```

## Request headers
|Header|Value|
|:---|:---|
|Authorization|Bearer &lt;token&gt; Required.|
|Accept|application/json|

## Request body
In the request body, supply a JSON representation for the [extendRemoteHelpSessionResponse](../resources/intune-remoteassistance-extendremotehelpsessionresponse.md) object.

The following table shows the properties that are required when you create the [extendRemoteHelpSessionResponse](../resources/intune-remoteassistance-extendremotehelpsessionresponse.md).

|Property|Type|Description|
|:---|:---|:---|
|sessionKey|String|The unique identifier for a session|
|acsHelperUserToken|String|Helper ACS User Token|
|pubSubHelperAccessUri|String|Azure Pubsub Group Id|
|sessionExpirationDateTime|DateTimeOffset|Azure Pubsub Session Expiration Date Time.|



## Response
If successful, this method returns a `200 OK` response code and an updated [extendRemoteHelpSessionResponse](../resources/intune-remoteassistance-extendremotehelpsessionresponse.md) object in the response body.

## Example

### Request
Here is an example of the request.
``` http
PATCH https://graph.microsoft.com/beta/ExtendRemoteHelpSessionResponse/{ExtendRemoteHelpSessionResponseId}
Content-type: application/json
Content-length: 299

{
  "@odata.type": "#microsoft.graph.extendRemoteHelpSessionResponse",
  "sessionKey": "Session Key value",
  "acsHelperUserToken": "Acs Helper User Token value",
  "pubSubHelperAccessUri": "Pub Sub Helper Access Uri value",
  "sessionExpirationDateTime": "2016-12-31T23:59:57.5564522-08:00"
}
```

### Response
Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 299

{
  "@odata.type": "#microsoft.graph.extendRemoteHelpSessionResponse",
  "sessionKey": "Session Key value",
  "acsHelperUserToken": "Acs Helper User Token value",
  "pubSubHelperAccessUri": "Pub Sub Helper Access Uri value",
  "sessionExpirationDateTime": "2016-12-31T23:59:57.5564522-08:00"
}
```
