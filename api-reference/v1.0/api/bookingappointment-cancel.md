---
title: "bookingAppointment: cancel"
description: "Cancel the specified bookingAppointment in the specified bookingBusiness and send a message to the involved customer and staff members."
ms.localizationpriority: medium
author: "arvindmicrosoft"
ms.prod: "bookings"
doc_type: apiPageType
---

# bookingAppointment: cancel

Namespace: microsoft.graph

Cancel the specified [bookingAppointment](../resources/bookingappointment.md) in the specified [bookingBusiness](../resources/bookingbusiness.md) and send a message to the involved customer and staff members.

## Permissions

Choose the permission or permissions marked as least privileged for this API. Use a higher privileged permission or permissions [only if your app requires it](/graph/permissions-overview#best-practices-for-using-microsoft-graph-permissions). For details about delegated and application permissions, see [Permission types](/graph/permissions-overview#permission-types). To learn more about these permissions, see the [permissions reference](/graph/permissions-reference).

<!-- { "blockType": "permissions", "name": "bookingappointment_cancel" } -->
[!INCLUDE [permissions-table](../includes/permissions/bookingappointment-cancel-permissions.md)]

## HTTP request
<!-- { "blockType": "ignored" } -->
```http
POST /solutions/bookingBusinesses/{id}/appointments/{id}/cancel
```

## Request headers

| Name       | Description|
|:---------------|:----------|
| Authorization  | Bearer {code}|

## Request body

In the request body, provide a JSON object with the following parameter.

| Parameter	   | Type	|Description|
|:---------------|:--------|:----------|
|cancellationMessage|String|A message to acknowledge with the customer that the **appointment** has been cancelled.|

## Response

If successful, this method returns a `204 No Content` response code. It does not return anything in the response body.

If you attempt to cancel an **appointment** that doesn't exist, this method returns `HTTP 404 Not Found`.

## Example

### Request

The following is an example of the request.

<!-- {
  "blockType": "request",
  "sampleKeys": ["AAMkADKoAAA=", "Contosolunchdelivery@contoso.onmicrosoft.com"]
}-->
```http
POST https://graph.microsoft.com/v1.0/solutions/bookingBusinesses/Contosolunchdelivery@contoso.onmicrosoft.com/appointments/AAMkADKoAAA=/cancel
Content-type: application/json

{
  "cancellationMessage": "Your appointment has been successfully cancelled. Please call us again."
}
```

### Response

The following is an example of the response.

<!-- {
  "blockType": "response"
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "bookingAppointment: cancel",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
  ]
}
-->
