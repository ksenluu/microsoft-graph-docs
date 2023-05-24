---
title: "Create deviceManagementConfigurationSetting"
description: "Create a new deviceManagementConfigurationSetting object."
author: "jaiprakashmb"
localization_priority: Normal
ms.prod: "intune"
doc_type: apiPageType
---

# Create deviceManagementConfigurationSetting

Namespace: microsoft.graph

> **Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.

> **Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.

Create a new [deviceManagementConfigurationSetting](../resources/intune-mam-devicemanagementconfigurationsetting.md) object.

## Permissions
Choose the permission or permissions marked as least privileged for this API. Use a higher privileged permission or permissions [only if your app requires it](/graph/permissions-overview#best-practices-for-using-microsoft-graph-permissions). For details about delegated and application permissions, see [Permission types](/graph/permissions-overview#permission-types). To learn more about these permissions, see the [permissions reference](/graph/permissions-reference).

<!-- { "blockType": "permissions", "name": "intune_mam_devicemanagementconfigurationsetting_create" } -->
[!INCLUDE [permissions-table](../includes/permissions/intune-mam-devicemanagementconfigurationsetting-create-permissions.md)]

## HTTP Request
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/targetedManagedAppConfigurations/{targetedManagedAppConfigurationId}/settings
```

## Request headers
|Header|Value|
|:---|:---|
|Authorization|Bearer &lt;token&gt; Required.|
|Accept|application/json|

## Request body
In the request body, supply a JSON representation for the deviceManagementConfigurationSetting object.

The following table shows the properties that are required when you create the deviceManagementConfigurationSetting.

|Property|Type|Description|
|:---|:---|:---|



## Response
If successful, this method returns a `201 Created` response code and a [deviceManagementConfigurationSetting](../resources/intune-mam-devicemanagementconfigurationsetting.md) object in the response body.

## Example

### Request
Here is an example of the request.
``` http
POST https://graph.microsoft.com/beta/deviceAppManagement/targetedManagedAppConfigurations/{targetedManagedAppConfigurationId}/settings
Content-type: application/json
Content-length: 78

{
  "@odata.type": "#microsoft.graph.deviceManagementConfigurationSetting"
}
```

### Response
Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 78

{
  "@odata.type": "#microsoft.graph.deviceManagementConfigurationSetting"
}
```
