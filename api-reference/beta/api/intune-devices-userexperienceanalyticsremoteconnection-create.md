---
title: "Create userExperienceAnalyticsRemoteConnection"
description: "Create a new userExperienceAnalyticsRemoteConnection object."
author: "jaiprakashmb"
localization_priority: Normal
ms.prod: "intune"
doc_type: apiPageType
---

# Create userExperienceAnalyticsRemoteConnection

Namespace: microsoft.graph

> **Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.

> **Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.

Create a new [userExperienceAnalyticsRemoteConnection](../resources/intune-devices-userexperienceanalyticsremoteconnection.md) object.

## Permissions
Choose the permission or permissions marked as least privileged for this API. Use a higher privileged permission or permissions [only if your app requires it](/graph/permissions-overview#best-practices-for-using-microsoft-graph-permissions). For details about delegated and application permissions, see [Permission types](/graph/permissions-overview#permission-types). To learn more about these permissions, see the [permissions reference](/graph/permissions-reference).

<!-- { "blockType": "permissions", "name": "intune_devices_userexperienceanalyticsremoteconnection_create" } -->
[!INCLUDE [permissions-table](../includes/permissions/intune-devices-userexperienceanalyticsremoteconnection-create-permissions.md)]

## HTTP Request
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/userExperienceAnalyticsRemoteConnection
```

## Request headers
|Header|Value|
|:---|:---|
|Authorization|Bearer &lt;token&gt; Required.|
|Accept|application/json|

## Request body
In the request body, supply a JSON representation for the userExperienceAnalyticsRemoteConnection object.

The following table shows the properties that are required when you create the userExperienceAnalyticsRemoteConnection.

|Property|Type|Description|
|:---|:---|:---|
|id|String|The unique identifier of the user experience analytics remote connection entity.|
|deviceId|String|The id of the device.|
|deviceName|String|The name of the device.|
|model|String|The user experience analytics device model.|
|virtualNetwork|String|The user experience analytics virtual network.|
|manufacturer|String|The user experience analytics manufacturer.|
|deviceCount|Int32|The count of remote connection. Valid values 0 to 2147483647|
|cloudPcRoundTripTime|Double|The round tip time of Cloud PC Device. Valid values 0 to 1.79769313486232E+308|
|cloudPcSignInTime|Double|The sign in time of Cloud PC Device. Valid values 0 to 1.79769313486232E+308|
|remoteSignInTime|Double|The remote sign in time of Cloud PC Device. Valid values 0 to 1.79769313486232E+308|
|coreBootTime|Double|The core boot time of Cloud PC Device. Valid values 0 to 1.79769313486232E+308|
|coreSignInTime|Double|The core sign in time of Cloud PC Device. Valid values 0 to 1.79769313486232E+308|
|cloudPcFailurePercentage|Double|The sign in failure percentage of Cloud PC Device. Valid values 0 to 100|
|userPrincipalName|String|The user experience analytics userPrincipalName.|



## Response
If successful, this method returns a `201 Created` response code and a [userExperienceAnalyticsRemoteConnection](../resources/intune-devices-userexperienceanalyticsremoteconnection.md) object in the response body.

## Example

### Request
Here is an example of the request.
``` http
POST https://graph.microsoft.com/beta/deviceManagement/userExperienceAnalyticsRemoteConnection
Content-type: application/json
Content-length: 573

{
  "@odata.type": "#microsoft.graph.userExperienceAnalyticsRemoteConnection",
  "deviceId": "Device Id value",
  "deviceName": "Device Name value",
  "model": "Model value",
  "virtualNetwork": "Virtual Network value",
  "manufacturer": "Manufacturer value",
  "deviceCount": 11,
  "cloudPcRoundTripTime": 6.666666666666667,
  "cloudPcSignInTime": 5.666666666666667,
  "remoteSignInTime": 5.333333333333333,
  "coreBootTime": 4.0,
  "coreSignInTime": 4.666666666666667,
  "cloudPcFailurePercentage": 8.0,
  "userPrincipalName": "User Principal Name value"
}
```

### Response
Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 622

{
  "@odata.type": "#microsoft.graph.userExperienceAnalyticsRemoteConnection",
  "id": "9ecbcf80-cf80-9ecb-80cf-cb9e80cfcb9e",
  "deviceId": "Device Id value",
  "deviceName": "Device Name value",
  "model": "Model value",
  "virtualNetwork": "Virtual Network value",
  "manufacturer": "Manufacturer value",
  "deviceCount": 11,
  "cloudPcRoundTripTime": 6.666666666666667,
  "cloudPcSignInTime": 5.666666666666667,
  "remoteSignInTime": 5.333333333333333,
  "coreBootTime": 4.0,
  "coreSignInTime": 4.666666666666667,
  "cloudPcFailurePercentage": 8.0,
  "userPrincipalName": "User Principal Name value"
}
```
