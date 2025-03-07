---
title: List software
description: Retrieves a list of software inventory
keywords: apis, graph api, supported apis, get, list, file, information, software inventory, threat & vulnerability management api, Microsoft Defender for Endpoint tvm api
search.product: eADQiWindows 10XVcnh
ms.prod: w10
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: dolmont
author: DulceMontemayor
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance 
ms.topic: article
MS.technology: mde
ms.custom: api
---

# List software inventory API

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

**Applies to:** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)

- Want to experience Microsoft Defender for Endpoint? [Sign up for a free trial.](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]

Retrieves the organization software inventory.

## Permissions
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Use Microsoft Defender for Endpoint APIs](apis-intro.md) for details.

Permission type |	Permission	|	Permission display name
:---|:---|:---
Application |Software.Read.All |	'Read Threat and Vulnerability Management Software information'
Delegated (work or school account) | Software.Read |	'Read Threat and Vulnerability Management Software information'

## HTTP request
```
GET /api/Software
```

## Request headers

Name | Type | Description
:---|:---|:---
Authorization | String | Bearer {token}. **Required**.


## Request body
Empty

## Response
If successful, this method returns 200 OK with the software inventory in the body.


## Example

**Request**

Here is an example of the request.

```
GET https://api.securitycenter.microsoft.com/api/Software
```

**Response**

Here is an example of the response.


```json
{
    "@odata.context": "https://api.securitycenter.microsoft.com/api/$metadata#Software",
    "value": [
			{
				"id": "microsoft-_-edge",
				"name": "edge",
				"vendor": "microsoft",
				"weaknesses": 467,
				"publicExploit": true,
				"activeAlert": false,
				"exposedMachines": 172,
				"impactScore": 2.39947438
			}
			...
        ]
}
```

## Related topics
- [Risk-based Threat & Vulnerability Management](/microsoft-365/security/defender-endpoint/next-gen-threat-and-vuln-mgt)
- [Threat & Vulnerability software inventory](/microsoft-365/security/defender-endpoint/tvm-software-inventory)
