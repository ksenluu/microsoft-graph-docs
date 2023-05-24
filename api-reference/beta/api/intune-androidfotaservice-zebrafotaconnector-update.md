---
title: "Update zebraFotaConnector"
description: "Update the properties of a zebraFotaConnector object."
author: "jaiprakashmb"
localization_priority: Normal
ms.prod: "intune"
doc_type: apiPageType
---

# Update zebraFotaConnector

Namespace: microsoft.graph

> **Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.

> **Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.

Update the properties of a [zebraFotaConnector](../resources/intune-androidfotaservice-zebrafotaconnector.md) object.

## Permissions
Choose the permission or permissions marked as least privileged for this API. Use a higher privileged permission or permissions [only if your app requires it](/graph/permissions-overview#best-practices-for-using-microsoft-graph-permissions). For details about delegated and application permissions, see [Permission types](/graph/permissions-overview#permission-types). To learn more about these permissions, see the [permissions reference](/graph/permissions-reference).

<!-- { "blockType": "permissions", "name": "intune_androidfotaservice_zebrafotaconnector_update" } -->
[!INCLUDE [permissions-table](../includes/permissions/intune-androidfotaservice-zebrafotaconnector-update-permissions.md)]

## HTTP Request
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/zebraFotaConnector
```

## Request headers
|Header|Value|
|:---|:---|
|Authorization|Bearer &lt;token&gt; Required.|
|Accept|application/json|

## Request body
In the request body, supply a JSON representation for the [zebraFotaConnector](../resources/intune-androidfotaservice-zebrafotaconnector.md) object.

The following table shows the properties that are required when you create the [zebraFotaConnector](../resources/intune-androidfotaservice-zebrafotaconnector.md).

|Property|Type|Description|
|:---|:---|:---|
|id|String|Id of ZebraFotaConnector.|
|state|[zebraFotaConnectorState](../resources/intune-androidfotaservice-zebrafotaconnectorstate.md)|The Zebra connector state. Possible values are: `none`, `connected`, `disconnected`, `unknownFutureValue`.|
|enrollmentToken|String|Tenant enrollment token from Zebra. The token is used to enroll Zebra devices in the FOTA Service via app config.|
|enrollmentAuthorizationUrl|String|Complete account enrollment authorization URL. This corresponds to verification_uri_complete in the Zebra API documentations.|
|lastSyncDateTime|DateTimeOffset|Date and time when the account was last synched with Zebra|
|fotaAppsApproved|Boolean|Flag indicating if required Firmware Over-the-Air (FOTA) Apps have been approved.|



## Response
If successful, this method returns a `200 OK` response code and an updated [zebraFotaConnector](../resources/intune-androidfotaservice-zebrafotaconnector.md) object in the response body.

## Example

### Request
Here is an example of the request.
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/zebraFotaConnector
Content-type: application/json
Content-length: 306

{
  "@odata.type": "#microsoft.graph.zebraFotaConnector",
  "state": "connected",
  "enrollmentToken": "Enrollment Token value",
  "enrollmentAuthorizationUrl": "https://example.com/enrollmentAuthorizationUrl/",
  "lastSyncDateTime": "2017-01-01T00:02:49.3205976-08:00",
  "fotaAppsApproved": true
}
```

### Response
Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 355

{
  "@odata.type": "#microsoft.graph.zebraFotaConnector",
  "id": "2301310a-310a-2301-0a31-01230a310123",
  "state": "connected",
  "enrollmentToken": "Enrollment Token value",
  "enrollmentAuthorizationUrl": "https://example.com/enrollmentAuthorizationUrl/",
  "lastSyncDateTime": "2017-01-01T00:02:49.3205976-08:00",
  "fotaAppsApproved": true
}
```
