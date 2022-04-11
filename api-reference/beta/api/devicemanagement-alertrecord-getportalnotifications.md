---
title: "alertRecord: getPortalNotifications"
description: "View a list of all portal notifications that are ready to be consumed for current user. The portal notifications can be used to publish MEM portal notifications."
author: "zhishending"
ms.localizationpriority: medium
ms.prod: "cloud-pc"
doc_type: apiPageType
---

# alertRecord: getPortalNotifications
Namespace: microsoft.graph.deviceManagement

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

View a list of all portal notifications that are ready to be consumed for current user. The portal notifications can be used to publish MEM portal notifications.

## Permissions
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

|Permission type|Permissions (from least to most privileged)|
|:---|:---|
|Delegated (work or school account)|CloudPC.Read.All, CloudPC.ReadWrite.All|
|Delegated (personal Microsoft account)|Not supported.|
|Application|CloudPC.Read.All, CloudPC.ReadWrite.All|

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/monitoring/alertRecords/getPortalNotifications
```

## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|

## Request body
Do not supply a request body for this method.

## Response

If successful, this function returns a `200 OK` response code and a [microsoft.graph.deviceManagement.portalNotification](../resources/devicemanagement-portalnotification.md) collection in the response body.

## Examples

### Request
<!-- {
  "blockType": "request",
  "name": "alertrecordthis.getportalnotifications"
}
-->
``` http
GET https://graph.microsoft.com/beta/deviceManagement/monitoring/alertRecords/getPortalNotifications
```

### Response
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "Collection(microsoft.graph.deviceManagement.portalNotification)"
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#Collection(microsoft.graph.deviceManagement.portalNotification)",
    "value": [
        {
            "id": "6575ceea-1d1c-48f1-b6af-01b98fbde246",
            "alertRuleId": "30070507-6514-443b-8fa5-06979cedacdf",
            "alertRecordId": "6c46a7ba-e78a-45e5-a81c-179ab8fd3e8e",
            "alertRuleName": "Upload failure for Device Images",
            "alertRuleTemplate": "cloudPcImageUploadScenario",
            "isPortalNotificationSent": true,
            "severity": "warning",
            "alertImpact": {
                "value": 2,
                "aggregationType": "count"
            }
        },
        {
            "id": "f2c9ef57-44b8-4783-87e6-e4131a9c1008",
            "alertRuleId": "215c55cc-b1c9-4d36-a870-be5778101714",
            "alertRecordId": "44336915-dfcb-479b-a4d6-54bd66fa1ad6",
            "alertRuleName": "Azure network connection failure impacting Cloud PCs",
            "alertRuleTemplate": "cloudPcOnPremiseNetworkConnectionCheckScenario",
            "isPortalNotificationSent": true,
            "severity": "warning",
            "alertImpact": {
                "value": 100,
                "aggregationType": "count"
            }
        }
    ]
}
```