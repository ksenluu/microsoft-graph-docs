---
title: "Get bookingCustomer"
description: "Get the properties and relationships of a bookingCustomer object."
ms.localizationpriority: medium
author: "arvindmicrosoft"
ms.prod: "bookings"
doc_type: apiPageType
---

# Get bookingCustomer

Namespace: microsoft.graph

Get the properties and relationships of a [bookingCustomer](../resources/bookingcustomer.md) object.

## Permissions

Choose the permission or permissions marked as least privileged for this API. Use a higher privileged permission or permissions [only if your app requires it](/graph/permissions-overview#best-practices-for-using-microsoft-graph-permissions). For details about delegated and application permissions, see [Permission types](/graph/permissions-overview#permission-types). To learn more about these permissions, see the [permissions reference](/graph/permissions-reference).

<!-- { "blockType": "permissions", "name": "bookingcustomer_get" } -->
[!INCLUDE [permissions-table](../includes/permissions/bookingcustomer-get-permissions.md)]

## HTTP request
<!-- { "blockType": "ignored" } -->
```http
GET /solutions/bookingBusinesses/{id}/customers/{id}
```
> **Note:** This method currently requires the ID to be Base64 encoded. GUID IDs do not work.

## Optional query parameters

This method supports the $count and $expand [OData query parameters](/graph/query-parameters) to help customize the response.

## Request headers

| Name      |Description|
|:----------|:----------|
| Authorization  | Bearer {code}|

## Request body

Do not supply a request body for this method.

## Response

If successful, this method returns a `200 OK` response code and a [bookingCustomer](../resources/bookingcustomer.md) object in the response body.

## Example

### Request

The following is an example of the request.

<!-- {
  "blockType": "request",
  "sampleKeys": ["Contosolunchdelivery@contoso.onmicrosoft.com", "8bb19078-0f45-4efb-b2c5-da78b860f73a"]
}-->
```http
GET https://graph.microsoft.com/v1.0/solutions/bookingBusinesses/Contosolunchdelivery@contoso.onmicrosoft.com/customers/8bb19078-0f45-4efb-b2c5-da78b860f73a
```

### Response

The following is an example of the response. 

>**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.bookingCustomer"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.type": "#microsoft.graph.bookingCustomer",
    "@odata.context": "https://graph.microsoft.com/v1.0/solutions/$metadata#bookingBusinesses('Contosolunchdelivery%40contoso.onmicrosoft.com')/customers/$entity",
    "id": "8bb19078-0f45-4efb-b2c5-da78b860f73a",
    "displayName": "Adele Vance",
    "emailAddress": "adelev@proseware.com",
    "addresses": [
        {
            "postOfficeBox":"",
            "street":"4567 Main Street",
            "city":"Buffalo",
            "state":"NY",
            "countryOrRegion":"USA",
            "postalCode":"98052",
            "type":"home"
        },
        {
            "postOfficeBox":"",
            "street":"4570 Main Street",
            "city":"Buffalo",
            "state":"NY",
            "countryOrRegion":"USA",
            "postalCode":"98054",
            "type":"business"
        }
    ],
    "phones": [
        {
            "number": "206-555-0100",
            "type": "home"
        },
        {
            "number": "206-555-0200",
            "type": "business"
        }
     ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "Get bookingCustomer",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
  ]
}
-->
