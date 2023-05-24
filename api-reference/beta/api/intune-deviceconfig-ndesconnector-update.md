---
title: "Update ndesConnector"
description: "Update the properties of a ndesConnector object."
author: "jaiprakashmb"
localization_priority: Normal
ms.prod: "intune"
doc_type: apiPageType
---

# Update ndesConnector

Namespace: microsoft.graph

> **Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.

> **Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.

Update the properties of a [ndesConnector](../resources/intune-deviceconfig-ndesconnector.md) object.

## Permissions
Choose the permission or permissions marked as least privileged for this API. Use a higher privileged permission or permissions [only if your app requires it](/graph/permissions-overview#best-practices-for-using-microsoft-graph-permissions). For details about delegated and application permissions, see [Permission types](/graph/permissions-overview#permission-types). To learn more about these permissions, see the [permissions reference](/graph/permissions-reference).

<!-- { "blockType": "permissions", "name": "intune_deviceconfig_ndesconnector_update" } -->
[!INCLUDE [permissions-table](../includes/permissions/intune-deviceconfig-ndesconnector-update-permissions.md)]

## HTTP Request
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/ndesConnectors/{ndesConnectorId}
```

## Request headers
|Header|Value|
|:---|:---|
|Authorization|Bearer &lt;token&gt; Required.|
|Accept|application/json|

## Request body
In the request body, supply a JSON representation for the [ndesConnector](../resources/intune-deviceconfig-ndesconnector.md) object.

The following table shows the properties that are required when you create the [ndesConnector](../resources/intune-deviceconfig-ndesconnector.md).

|Property|Type|Description|
|:---|:---|:---|
|id|String|The key of the NDES Connector.|
|lastConnectionDateTime|DateTimeOffset|Last connection time for the Ndes Connector|
|state|[ndesConnectorState](../resources/intune-deviceconfig-ndesconnectorstate.md)|Ndes Connector Status. Possible values are: `none`, `active`, `inactive`.|
|displayName|String|The friendly name of the Ndes Connector.|
|machineName|String|Name of the machine running on-prem certificate connector service.|
|enrolledDateTime|DateTimeOffset|Timestamp when on-prem certificate connector was enrolled in Intune.|
|roleScopeTagIds|String collection|List of Scope Tags for this Entity instance.|
|connectorVersion|String|The build version of the Ndes Connector.|



## Response
If successful, this method returns a `200 OK` response code and an updated [ndesConnector](../resources/intune-deviceconfig-ndesconnector.md) object in the response body.

## Example

### Request
Here is an example of the request.
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/ndesConnectors/{ndesConnectorId}
Content-type: application/json
Content-length: 394

{
  "@odata.type": "#microsoft.graph.ndesConnector",
  "lastConnectionDateTime": "2016-12-31T23:58:36.6670033-08:00",
  "state": "active",
  "displayName": "Display Name value",
  "machineName": "Machine Name value",
  "enrolledDateTime": "2016-12-31T23:59:43.797191-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "connectorVersion": "Connector Version value"
}
```

### Response
Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 443

{
  "@odata.type": "#microsoft.graph.ndesConnector",
  "id": "e71fa706-a706-e71f-06a7-1fe706a71fe7",
  "lastConnectionDateTime": "2016-12-31T23:58:36.6670033-08:00",
  "state": "active",
  "displayName": "Display Name value",
  "machineName": "Machine Name value",
  "enrolledDateTime": "2016-12-31T23:59:43.797191-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "connectorVersion": "Connector Version value"
}
```
