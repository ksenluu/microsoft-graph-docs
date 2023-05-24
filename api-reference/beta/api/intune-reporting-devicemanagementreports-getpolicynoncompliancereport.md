---
title: "getPolicyNonComplianceReport action"
description: "Not yet documented"
author: "jaiprakashmb"
localization_priority: Normal
ms.prod: "intune"
doc_type: apiPageType
---

# getPolicyNonComplianceReport action

Namespace: microsoft.graph

> **Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.

> **Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.

Not yet documented

## Permissions
Choose the permission or permissions marked as least privileged for this API. Use a higher privileged permission or permissions [only if your app requires it](/graph/permissions-overview#best-practices-for-using-microsoft-graph-permissions). For details about delegated and application permissions, see [Permission types](/graph/permissions-overview#permission-types). To learn more about these permissions, see the [permissions reference](/graph/permissions-reference).

<!-- { "blockType": "permissions", "name": "intune_reporting_devicemanagementreports_getpolicynoncompliancereport" } -->
[!INCLUDE [permissions-table](../includes/permissions/intune-reporting-devicemanagementreports-getpolicynoncompliancereport-permissions.md)]

## HTTP Request
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/reports/getPolicyNonComplianceReport
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
|name|String|Not yet documented|
|select|String collection|Not yet documented|
|search|String|Not yet documented|
|groupBy|String collection|Not yet documented|
|orderBy|String collection|Not yet documented|
|skip|Int32|Not yet documented|
|top|Int32|Not yet documented|
|sessionId|String|Not yet documented|
|filter|String|Not yet documented|



## Response
If successful, this action returns a `200 OK` response code and a Stream in the response body.

## Example

### Request
Here is an example of the request.
``` http
POST https://graph.microsoft.com/beta/deviceManagement/reports/getPolicyNonComplianceReport

Content-type: application/json
Content-length: 278

{
  "name": "Name value",
  "select": [
    "Select value"
  ],
  "search": "Search value",
  "groupBy": [
    "Group By value"
  ],
  "orderBy": [
    "Order By value"
  ],
  "skip": 4,
  "top": 3,
  "sessionId": "Session Id value",
  "filter": "Filter value"
}
```

### Response
Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 95

{
  "value": "Z2V0UG9saWN5Tm9uQ29tcGxpYW5jZVJlcG9ydCBJbnR1bmUgRG9jIFNhbXBsZSAtNjU2NTI5OTUw"
}
```
