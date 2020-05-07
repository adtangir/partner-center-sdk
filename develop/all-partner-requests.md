---
title: Get a list of all partner user requests
description: Obtains a list of all partner user requests
ms.date: 05/03/2020
ms.service: partner-dashboard
ms.subservice: partnercenter-sdk
ms.localizationpriority: medium
---

# Get all partner requests

Applies to:

- Partner Center API

This topic explains how to obtain a list of all partner user requests within a tenant. 

## Prerequisites

- Credentials as described in [Partner API authentication](api-authentication.md). This scenario supports authentication with App+User credentials.

## REST Request

### Request syntax

| Method  | Request URI                                                        |
|---------|--------------------------------------------------------------------|
| **GET** | <https://api.partnercenter.microsoft.com/pcapi/v1/partnerRequests> |

### Request headers

- See [Partner API REST headers](headers.md) for more information.

### Request example

```http
GET https://api.partnercenter.microsoft.com/pcapi/v1/partnerRequests HTTP/1.1
Authorization: Bearer <token>
Host: api.partnercenter.microsoft.com
Content-Type: application/json
```

## REST Response

If successful, this method returns a response containing the following fields.

### Response body

This table describes the properties in the response body for a non MFA compliant partner principals.

| Property                            | Type            | Description               |
|-------------------------------------|-----------------|---------------------------|
| RequestId                           | string          |                           |
| CorrelationId                       | string          |                           |
| OperationName                       | string          |                           |
| RequestDateTime                     | DateTime        |                           |
| IpAddress                           | string          |                           |
| ObjectId                            | string          |                           |
| TenantId                            | string          |                           |
| Upn                                 | string          |                           |
| ApplicationId                       | string          |                           |
| MfaCompliant                        | bool            |                           |

### Response success and error codes

Each response comes with an HTTP status code that indicates success or failure and additional debugging information. Use a network trace tool to read this code, error type, and additional parameters. For the full list, see [Error Codes](error-codes.md).

### Response example

``` http
  {
    "requestId": "",
    "correlationId": "",
    "operationName": "",
    "requestDateTime": "",
    "ipAddress": "",
    "objectId": "",
    "tenantId": "",
    "upn": "",
    "applicationId": "",
    "mfaCompliant": ""
  }
```
