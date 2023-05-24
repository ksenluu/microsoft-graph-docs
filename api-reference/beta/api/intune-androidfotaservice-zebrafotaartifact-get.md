---
title: "Get zebraFotaArtifact"
description: "Read properties and relationships of the zebraFotaArtifact object."
author: "jaiprakashmb"
localization_priority: Normal
ms.prod: "intune"
doc_type: apiPageType
---

# Get zebraFotaArtifact

Namespace: microsoft.graph

> **Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.

> **Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.

Read properties and relationships of the [zebraFotaArtifact](../resources/intune-androidfotaservice-zebrafotaartifact.md) object.

## Permissions
Choose the permission or permissions marked as least privileged for this API. Use a higher privileged permission or permissions [only if your app requires it](/graph/permissions-overview#best-practices-for-using-microsoft-graph-permissions). For details about delegated and application permissions, see [Permission types](/graph/permissions-overview#permission-types). To learn more about these permissions, see the [permissions reference](/graph/permissions-reference).

<!-- { "blockType": "permissions", "name": "intune_androidfotaservice_zebrafotaartifact_get" } -->
[!INCLUDE [permissions-table](../includes/permissions/intune-androidfotaservice-zebrafotaartifact-get-permissions.md)]

## HTTP Request
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/zebraFotaArtifacts/{zebraFotaArtifactId}
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
If successful, this method returns a `200 OK` response code and [zebraFotaArtifact](../resources/intune-androidfotaservice-zebrafotaartifact.md) object in the response body.

## Example

### Request
Here is an example of the request.
``` http
GET https://graph.microsoft.com/beta/deviceManagement/zebraFotaArtifacts/{zebraFotaArtifactId}
```

### Response
Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 434

{
  "value": {
    "@odata.type": "#microsoft.graph.zebraFotaArtifact",
    "id": "37305f61-5f61-3730-615f-3037615f3037",
    "deviceModel": "Device Model value",
    "osVersion": "Os Version value",
    "patchVersion": "Patch Version value",
    "boardSupportPackageVersion": "Board Support Package Version value",
    "releaseNotesUrl": "https://example.com/releaseNotesUrl/",
    "description": "Description value"
  }
}
```
