---
title: "List deviceManagementConfigurationPolicyTemplates"
description: "List properties and relationships of the deviceManagementConfigurationPolicyTemplate objects."
author: "jaiprakashmb"
localization_priority: Normal
ms.prod: "intune"
doc_type: apiPageType
---

# List deviceManagementConfigurationPolicyTemplates

Namespace: microsoft.graph

> **Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.

> **Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.

List properties and relationships of the [deviceManagementConfigurationPolicyTemplate](../resources/intune-deviceconfigv2-devicemanagementconfigurationpolicytemplate.md) objects.

## Permissions
Choose the permission or permissions marked as least privileged for this API. Use a higher privileged permission or permissions [only if your app requires it](/graph/permissions-overview#best-practices-for-using-microsoft-graph-permissions). For details about delegated and application permissions, see [Permission types](/graph/permissions-overview#permission-types). To learn more about these permissions, see the [permissions reference](/graph/permissions-reference).

<!-- { "blockType": "permissions", "name": "intune_deviceconfigv2_devicemanagementconfigurationpolicytemplate_list" } -->
[!INCLUDE [permissions-table](../includes/permissions/intune-deviceconfigv2-devicemanagementconfigurationpolicytemplate-list-permissions.md)]

## HTTP Request
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/configurationPolicyTemplates
```

## Request headers
|Header|Value|
|:---|:---|
|Authorization|Bearer &lt;token&gt; Required.|
|Accept|application/json|

## Request body
Do not supply a request body for this method.

## Response
If successful, this method returns a `200 OK` response code and a collection of [deviceManagementConfigurationPolicyTemplate](../resources/intune-deviceconfigv2-devicemanagementconfigurationpolicytemplate.md) objects in the response body.

## Example

### Request
Here is an example of the request.
``` http
GET https://graph.microsoft.com/beta/deviceManagement/configurationPolicyTemplates
```

### Response
Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 589

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.deviceManagementConfigurationPolicyTemplate",
      "id": "424ddb9a-db9a-424d-9adb-4d429adb4d42",
      "baseId": "Base Id value",
      "version": 7,
      "displayName": "Display Name value",
      "description": "Description value",
      "displayVersion": "Display Version value",
      "lifecycleState": "draft",
      "platforms": "android",
      "technologies": "mdm",
      "templateFamily": "endpointSecurityAntivirus",
      "allowUnmanagedSettings": true,
      "settingTemplateCount": 4
    }
  ]
}
```
