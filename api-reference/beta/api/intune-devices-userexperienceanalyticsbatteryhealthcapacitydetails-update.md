---
title: "Update userExperienceAnalyticsBatteryHealthCapacityDetails"
description: "Update the properties of a userExperienceAnalyticsBatteryHealthCapacityDetails object."
author: "jaiprakashmb"
localization_priority: Normal
ms.prod: "intune"
doc_type: apiPageType
---

# Update userExperienceAnalyticsBatteryHealthCapacityDetails

Namespace: microsoft.graph

> **Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.

> **Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.

Update the properties of a [userExperienceAnalyticsBatteryHealthCapacityDetails](../resources/intune-devices-userexperienceanalyticsbatteryhealthcapacitydetails.md) object.

## Permissions
Choose the permission or permissions marked as least privileged for this API. Use a higher privileged permission or permissions [only if your app requires it](/graph/permissions-overview#best-practices-for-using-microsoft-graph-permissions). For details about delegated and application permissions, see [Permission types](/graph/permissions-overview#permission-types). To learn more about these permissions, see the [permissions reference](/graph/permissions-reference).

<!-- { "blockType": "permissions", "name": "intune_devices_userexperienceanalyticsbatteryhealthcapacitydetails_update" } -->
[!INCLUDE [permissions-table](../includes/permissions/intune-devices-userexperienceanalyticsbatteryhealthcapacitydetails-update-permissions.md)]

## HTTP Request
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/userExperienceAnalyticsBatteryHealthCapacityDetails
```

## Request headers
|Header|Value|
|:---|:---|
|Authorization|Bearer &lt;token&gt; Required.|
|Accept|application/json|

## Request body
In the request body, supply a JSON representation for the [userExperienceAnalyticsBatteryHealthCapacityDetails](../resources/intune-devices-userexperienceanalyticsbatteryhealthcapacitydetails.md) object.

The following table shows the properties that are required when you create the [userExperienceAnalyticsBatteryHealthCapacityDetails](../resources/intune-devices-userexperienceanalyticsbatteryhealthcapacitydetails.md).

|Property|Type|Description|
|:---|:---|:---|
|id|String|The unique identifier of the user experience analytics battery health capacity object.|
|activeDevices|Int32|Number of active devices within the tenant. Valid values -2147483648 to 2147483647|
|batteryCapacityGood|Int32|Number of devices whose battery maximum capacity is greater than 80%. Valid values -2147483648 to 2147483647|
|batteryCapacityFair|Int32|Number of devices whose battery maximum capacity is greater than 50% but lesser than 80%. Valid values -2147483648 to 2147483647|
|batteryCapacityPoor|Int32|Number of devices whose battery maximum capacity is lesser than 50%. Valid values -2147483648 to 2147483647|
|lastRefreshedDateTime|DateTimeOffset|Recorded date time of this capacity details instance.|



## Response
If successful, this method returns a `200 OK` response code and an updated [userExperienceAnalyticsBatteryHealthCapacityDetails](../resources/intune-devices-userexperienceanalyticsbatteryhealthcapacitydetails.md) object in the response body.

## Example

### Request
Here is an example of the request.
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/userExperienceAnalyticsBatteryHealthCapacityDetails
Content-type: application/json
Content-length: 269

{
  "@odata.type": "#microsoft.graph.userExperienceAnalyticsBatteryHealthCapacityDetails",
  "activeDevices": 13,
  "batteryCapacityGood": 3,
  "batteryCapacityFair": 3,
  "batteryCapacityPoor": 3,
  "lastRefreshedDateTime": "2017-01-01T00:02:37.7100903-08:00"
}
```

### Response
Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 318

{
  "@odata.type": "#microsoft.graph.userExperienceAnalyticsBatteryHealthCapacityDetails",
  "id": "b01fc7df-c7df-b01f-dfc7-1fb0dfc71fb0",
  "activeDevices": 13,
  "batteryCapacityGood": 3,
  "batteryCapacityFair": 3,
  "batteryCapacityPoor": 3,
  "lastRefreshedDateTime": "2017-01-01T00:02:37.7100903-08:00"
}
```
