---
title: "Update remoteAssistanceSettings"
description: "Update the properties of a remoteAssistanceSettings object."
author: "jaiprakashmb"
localization_priority: Normal
ms.prod: "intune"
doc_type: apiPageType
---

# Update remoteAssistanceSettings

Namespace: microsoft.graph

> **Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.

> **Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.

Update the properties of a [remoteAssistanceSettings](../resources/intune-remoteassistance-remoteassistancesettings.md) object.

## Permissions
Choose the permission or permissions marked as least privileged for this API. Use a higher privileged permission or permissions [only if your app requires it](/graph/permissions-overview#best-practices-for-using-microsoft-graph-permissions). For details about delegated and application permissions, see [Permission types](/graph/permissions-overview#permission-types). To learn more about these permissions, see the [permissions reference](/graph/permissions-reference).

<!-- { "blockType": "permissions", "name": "intune_remoteassistance_remoteassistancesettings_update" } -->
[!INCLUDE [permissions-table](../includes/permissions/intune-remoteassistance-remoteassistancesettings-update-permissions.md)]

## HTTP Request
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/remoteAssistanceSettings
```

## Request headers
|Header|Value|
|:---|:---|
|Authorization|Bearer &lt;token&gt; Required.|
|Accept|application/json|

## Request body
In the request body, supply a JSON representation for the [remoteAssistanceSettings](../resources/intune-remoteassistance-remoteassistancesettings.md) object.

The following table shows the properties that are required when you create the [remoteAssistanceSettings](../resources/intune-remoteassistance-remoteassistancesettings.md).

|Property|Type|Description|
|:---|:---|:---|
|id|String|The remote assistance settings identifier|
|remoteAssistanceState|[remoteAssistanceState](../resources/intune-remoteassistance-remoteassistancestate.md)|The current state of remote assistance for the account. Possible values are: disabled, enabled. This setting is configurable by the admin. Remote assistance settings that have not yet been configured by the admin have a disabled state. Returned by default. Possible values are: `disabled`, `enabled`.|
|allowSessionsToUnenrolledDevices|Boolean| Indicates if sessions to unenrolled devices are allowed for the account. This setting is configurable by the admin. Default value is false.|
|blockChat|Boolean| Indicates if sessions to block chat function. This setting is configurable by the admin. Default value is false.|



## Response
If successful, this method returns a `200 OK` response code and an updated [remoteAssistanceSettings](../resources/intune-remoteassistance-remoteassistancesettings.md) object in the response body.

## Example

### Request
Here is an example of the request.
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/remoteAssistanceSettings
Content-type: application/json
Content-length: 172

{
  "@odata.type": "#microsoft.graph.remoteAssistanceSettings",
  "remoteAssistanceState": "enabled",
  "allowSessionsToUnenrolledDevices": true,
  "blockChat": true
}
```

### Response
Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 221

{
  "@odata.type": "#microsoft.graph.remoteAssistanceSettings",
  "id": "cfef360e-360e-cfef-0e36-efcf0e36efcf",
  "remoteAssistanceState": "enabled",
  "allowSessionsToUnenrolledDevices": true,
  "blockChat": true
}
```
