---
title: "Create userExperienceAnalyticsAppHealthDeviceModelPerformance"
description: "Create a new userExperienceAnalyticsAppHealthDeviceModelPerformance object."
author: "jaiprakashmb"
localization_priority: Normal
ms.prod: "intune"
doc_type: apiPageType
---

# Create userExperienceAnalyticsAppHealthDeviceModelPerformance

Namespace: microsoft.graph

> **Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.

> **Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.

Create a new [userExperienceAnalyticsAppHealthDeviceModelPerformance](../resources/intune-devices-userexperienceanalyticsapphealthdevicemodelperformance.md) object.

## Permissions
Choose the permission or permissions marked as least privileged for this API. Use a higher privileged permission or permissions [only if your app requires it](/graph/permissions-overview#best-practices-for-using-microsoft-graph-permissions). For details about delegated and application permissions, see [Permission types](/graph/permissions-overview#permission-types). To learn more about these permissions, see the [permissions reference](/graph/permissions-reference).

<!-- { "blockType": "permissions", "name": "intune_devices_userexperienceanalyticsapphealthdevicemodelperformance_create" } -->
[!INCLUDE [permissions-table](../includes/permissions/intune-devices-userexperienceanalyticsapphealthdevicemodelperformance-create-permissions.md)]

## HTTP Request
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/userExperienceAnalyticsAppHealthDeviceModelPerformance
```

## Request headers
|Header|Value|
|:---|:---|
|Authorization|Bearer &lt;token&gt; Required.|
|Accept|application/json|

## Request body
In the request body, supply a JSON representation for the userExperienceAnalyticsAppHealthDeviceModelPerformance object.

The following table shows the properties that are required when you create the userExperienceAnalyticsAppHealthDeviceModelPerformance.

|Property|Type|Description|
|:---|:---|:---|
|id|String|The unique identifier of the user experience analytics device model performance object.|
|deviceModel|String|The model name of the device.|
|deviceManufacturer|String|The manufacturer name of the device.|
|activeDeviceCount|Int32|The number of active devices for the model. Valid values -2147483648 to 2147483647|
|meanTimeToFailureInMinutes|Int32|The mean time to failure for the model device in minutes. Valid values -2147483648 to 2147483647|
|modelAppHealthScore|Double|The app health score of the device model. Valid values -1.79769313486232E+308 to 1.79769313486232E+308|
|modelAppHealthStatus|String|The overall app health status of the device model.|
|healthStatus|[userExperienceAnalyticsHealthState](../resources/intune-devices-userexperienceanalyticshealthstate.md)|The health state of the user experience analytics model. Possible values are: `unknown`, `insufficientData`, `needsAttention`, `meetingGoals`, `unknownFutureValue`.|



## Response
If successful, this method returns a `201 Created` response code and a [userExperienceAnalyticsAppHealthDeviceModelPerformance](../resources/intune-devices-userexperienceanalyticsapphealthdevicemodelperformance.md) object in the response body.

## Example

### Request
Here is an example of the request.
``` http
POST https://graph.microsoft.com/beta/deviceManagement/userExperienceAnalyticsAppHealthDeviceModelPerformance
Content-type: application/json
Content-length: 398

{
  "@odata.type": "#microsoft.graph.userExperienceAnalyticsAppHealthDeviceModelPerformance",
  "deviceModel": "Device Model value",
  "deviceManufacturer": "Device Manufacturer value",
  "activeDeviceCount": 1,
  "meanTimeToFailureInMinutes": 10,
  "modelAppHealthScore": 6.333333333333333,
  "modelAppHealthStatus": "Model App Health Status value",
  "healthStatus": "insufficientData"
}
```

### Response
Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 447

{
  "@odata.type": "#microsoft.graph.userExperienceAnalyticsAppHealthDeviceModelPerformance",
  "id": "4daddc60-dc60-4dad-60dc-ad4d60dcad4d",
  "deviceModel": "Device Model value",
  "deviceManufacturer": "Device Manufacturer value",
  "activeDeviceCount": 1,
  "meanTimeToFailureInMinutes": 10,
  "modelAppHealthScore": 6.333333333333333,
  "modelAppHealthStatus": "Model App Health Status value",
  "healthStatus": "insufficientData"
}
```
