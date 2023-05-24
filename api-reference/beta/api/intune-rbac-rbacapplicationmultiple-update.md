---
title: "Update rbacApplicationMultiple"
description: "Update the properties of a rbacApplicationMultiple object."
author: "jaiprakashmb"
localization_priority: Normal
ms.prod: "intune"
doc_type: apiPageType
---

# Update rbacApplicationMultiple

Namespace: microsoft.graph

> **Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.

> **Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.

Update the properties of a [rbacApplicationMultiple](../resources/intune-rbac-rbacapplicationmultiple.md) object.

## Permissions
Choose the permission or permissions marked as least privileged for this API. Use a higher privileged permission or permissions [only if your app requires it](/graph/permissions-overview#best-practices-for-using-microsoft-graph-permissions). For details about delegated and application permissions, see [Permission types](/graph/permissions-overview#permission-types). To learn more about these permissions, see the [permissions reference](/graph/permissions-reference).

<!-- { "blockType": "permissions", "name": "intune_rbac_rbacapplicationmultiple_update" } -->
[!INCLUDE [permissions-table](../includes/permissions/intune-rbac-rbacapplicationmultiple-update-permissions.md)]

## HTTP Request
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /roleManagement/deviceManagement
```

## Request headers
|Header|Value|
|:---|:---|
|Authorization|Bearer &lt;token&gt; Required.|
|Accept|application/json|

## Request body
In the request body, supply a JSON representation for the [rbacApplicationMultiple](../resources/intune-rbac-rbacapplicationmultiple.md) object.

The following table shows the properties that are required when you create the [rbacApplicationMultiple](../resources/intune-rbac-rbacapplicationmultiple.md).

|Property|Type|Description|
|:---|:---|:---|
|id|String|Not yet documented|



## Response
If successful, this method returns a `200 OK` response code and an updated [rbacApplicationMultiple](../resources/intune-rbac-rbacapplicationmultiple.md) object in the response body.

## Example

### Request
Here is an example of the request.
``` http
PATCH https://graph.microsoft.com/beta/roleManagement/deviceManagement
Content-type: application/json
Content-length: 65

{
  "@odata.type": "#microsoft.graph.rbacApplicationMultiple"
}
```

### Response
Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 114

{
  "@odata.type": "#microsoft.graph.rbacApplicationMultiple",
  "id": "ee4797e5-97e5-ee47-e597-47eee59747ee"
}
```
