---
title: "evaluateAssignmentFilter action"
description: "Not yet documented"
author: "jaiprakashmb"
localization_priority: Normal
ms.prod: "intune"
doc_type: apiPageType
---

# evaluateAssignmentFilter action

Namespace: microsoft.graph

> **Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.

> **Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.

Not yet documented

## Permissions
Choose the permission or permissions marked as least privileged for this API. Use a higher privileged permission or permissions [only if your app requires it](/graph/permissions-overview#best-practices-for-using-microsoft-graph-permissions). For details about delegated and application permissions, see [Permission types](/graph/permissions-overview#permission-types). To learn more about these permissions, see the [permissions reference](/graph/permissions-reference).

<!-- { "blockType": "permissions", "name": "intune_policyset_devicemanagement_evaluateassignmentfilter" } -->
[!INCLUDE [permissions-table](../includes/permissions/intune-policyset-devicemanagement-evaluateassignmentfilter-permissions.md)]

## HTTP Request
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/evaluateAssignmentFilter
```

## Request headers
|Header|Value|
|:---|:---|
|Authorization|Bearer &lt;token&gt; Required.|
|Accept|application/json|

## Request body
In the request body, supply JSON representation of the parameters.

The following table shows the parameters that can be used with this action.

|Property|Type|Description|
|:---|:---|:---|
|data|[assignmentFilterEvaluateRequest](../resources/intune-policyset-assignmentfilterevaluaterequest.md)|Not yet documented|



## Response
If successful, this action returns a `200 OK` response code and a Stream in the response body.

## Example

### Request
Here is an example of the request.
``` http
POST https://graph.microsoft.com/beta/deviceManagement/evaluateAssignmentFilter

Content-type: application/json
Content-length: 266

{
  "data": {
    "@odata.type": "microsoft.graph.assignmentFilterEvaluateRequest",
    "platform": "androidForWork",
    "rule": "Rule value",
    "top": 3,
    "skip": 4,
    "orderBy": [
      "Order By value"
    ],
    "search": "Search value"
  }
}
```

### Response
Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 91

{
  "value": "ZXZhbHVhdGVBc3NpZ25tZW50RmlsdGVyIEludHVuZSBEb2MgU2FtcGxlIC0yNTU4NTk4OTA="
}
```
