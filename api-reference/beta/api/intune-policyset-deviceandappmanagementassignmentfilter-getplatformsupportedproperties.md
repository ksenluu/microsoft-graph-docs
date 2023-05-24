---
title: "getPlatformSupportedProperties function"
description: "Not yet documented"
author: "jaiprakashmb"
localization_priority: Normal
ms.prod: "intune"
doc_type: apiPageType
---

# getPlatformSupportedProperties function

Namespace: microsoft.graph

> **Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.

> **Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.

Not yet documented

## Permissions
Choose the permission or permissions marked as least privileged for this API. Use a higher privileged permission or permissions [only if your app requires it](/graph/permissions-overview#best-practices-for-using-microsoft-graph-permissions). For details about delegated and application permissions, see [Permission types](/graph/permissions-overview#permission-types). To learn more about these permissions, see the [permissions reference](/graph/permissions-reference).

<!-- { "blockType": "permissions", "name": "intune_policyset_deviceandappmanagementassignmentfilter_getplatformsupportedproperties" } -->
[!INCLUDE [permissions-table](../includes/permissions/intune-policyset-deviceandappmanagementassignmentfilter-getplatformsupportedproperties-permissions.md)]

## HTTP Request
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/assignmentFilters/getPlatformSupportedProperties
```

## Request headers
|Header|Value|
|:---|:---|
|Authorization|Bearer &lt;token&gt; Required.|
|Accept|application/json|

## Request body
In the request URL, provide the following query parameters with values.
The following table shows the parameters that can be used with this function.

|Property|Type|Description|
|:---|:---|:---|
|platform|[devicePlatformType](../resources/intune-policyset-deviceplatformtype.md)|Not yet documented|



## Response
If successful, this function returns a `200 OK` response code and a [assignmentFilterSupportedProperty](../resources/intune-policyset-assignmentfiltersupportedproperty.md) collection in the response body.

## Example

### Request
Here is an example of the request.
``` http
GET https://graph.microsoft.com/beta/deviceManagement/assignmentFilters/getPlatformSupportedProperties(platform='parameterValue')
```

### Response
Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 407

{
  "value": [
    {
      "@odata.type": "microsoft.graph.assignmentFilterSupportedProperty",
      "dataType": "Data Type value",
      "isCollection": true,
      "name": "Name value",
      "propertyRegexConstraint": "Property Regex Constraint value",
      "supportedOperators": [
        "equals"
      ],
      "supportedValues": [
        "Supported Values value"
      ]
    }
  ]
}
```
