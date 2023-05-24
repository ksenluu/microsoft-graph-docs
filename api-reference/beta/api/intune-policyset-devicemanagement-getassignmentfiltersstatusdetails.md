---
title: "getAssignmentFiltersStatusDetails action"
description: "Not yet documented"
author: "jaiprakashmb"
localization_priority: Normal
ms.prod: "intune"
doc_type: apiPageType
---

# getAssignmentFiltersStatusDetails action

Namespace: microsoft.graph

> **Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.

> **Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.

Not yet documented

## Permissions
Choose the permission or permissions marked as least privileged for this API. Use a higher privileged permission or permissions [only if your app requires it](/graph/permissions-overview#best-practices-for-using-microsoft-graph-permissions). For details about delegated and application permissions, see [Permission types](/graph/permissions-overview#permission-types). To learn more about these permissions, see the [permissions reference](/graph/permissions-reference).

<!-- { "blockType": "permissions", "name": "intune_policyset_devicemanagement_getassignmentfiltersstatusdetails" } -->
[!INCLUDE [permissions-table](../includes/permissions/intune-policyset-devicemanagement-getassignmentfiltersstatusdetails-permissions.md)]

## HTTP Request
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/getAssignmentFiltersStatusDetails
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
|managedDeviceId|String|Not yet documented|
|payloadId|String|Not yet documented|
|userId|String|Not yet documented|
|assignmentFilterIds|String collection|Not yet documented|
|top|Int32|Not yet documented|
|skip|Int32|Not yet documented|



## Response
If successful, this action returns a `200 OK` response code and a [assignmentFilterStatusDetails](../resources/intune-policyset-assignmentfilterstatusdetails.md) in the response body.

## Example

### Request
Here is an example of the request.
``` http
POST https://graph.microsoft.com/beta/deviceManagement/getAssignmentFiltersStatusDetails

Content-type: application/json
Content-length: 214

{
  "managedDeviceId": "Managed Device Id value",
  "payloadId": "Payload Id value",
  "userId": "User Id value",
  "assignmentFilterIds": [
    "Assignment Filter Ids value"
  ],
  "top": 3,
  "skip": 4
}
```

### Response
Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1216

{
  "value": {
    "@odata.type": "microsoft.graph.assignmentFilterStatusDetails",
    "managedDeviceId": "Managed Device Id value",
    "payloadId": "Payload Id value",
    "userId": "User Id value",
    "deviceProperties": [
      {
        "@odata.type": "microsoft.graph.keyValuePair",
        "name": "Name value",
        "value": "Value value"
      }
    ],
    "evalutionSummaries": [
      {
        "@odata.type": "microsoft.graph.assignmentFilterEvaluationSummary",
        "assignmentFilterId": "Assignment Filter Id value",
        "assignmentFilterLastModifiedDateTime": "2017-01-01T00:02:50.0900701-08:00",
        "assignmentFilterDisplayName": "Assignment Filter Display Name value",
        "assignmentFilterPlatform": "androidForWork",
        "evaluationResult": "match",
        "evaluationDateTime": "2016-12-31T23:58:01.2047675-08:00",
        "assignmentFilterType": "include",
        "assignmentFilterTypeAndEvaluationResults": [
          {
            "@odata.type": "microsoft.graph.assignmentFilterTypeAndEvaluationResult",
            "assignmentFilterType": "include",
            "evaluationResult": "match"
          }
        ]
      }
    ]
  }
}
```
