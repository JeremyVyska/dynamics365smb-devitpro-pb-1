---
title: Update picture  
description: A picture object in Dynamics 365 Business Central. 
 
author: SusanneWindfeldPedersen

ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 04/01/2021
ms.author: solsen
---

# Update picture

[!INCLUDE[api_v2_note](../../../includes/api_v2_note.md)]

Updates the properties and relationships of a picture object for [!INCLUDE[prod_short](../../../includes/prod_short.md)].

## HTTP request
Replace the URL prefix for [!INCLUDE[prod_short](../../../includes/prod_short.md)] depending on environment following the [guideline](../../v2.0/endpoints-apis-for-dynamics.md).
```
PATCH businesscentralPrefix/companies({companyId})/items({itemId})/picture({pictureId})/content
PATCH businesscentralPrefix/companies({companyId})/vendors({vendorId})/picture({pictureId})/content
PATCH businesscentralPrefix/companies({companyId})/employees({employeeId})/picture({pictureId})/content
PATCH businesscentralPrefix/companies({companyId})/customers({customerId})/picture({pictureId})/content

```

## Request headers

|Header|Value|
|------|-----|
|Authorization  |Bearer {token}. Required. |
|Content-Type  |application/octet-stream  | 
|If Match | When this request header is included and the eTag provided does not match the current tag on the picture, the picture will not be updated.|

## Request body
Raw picture binary data.

## Response
If successful, this method returns `204 No Content` response code. It does not return anything in the response body.

## Example

**Request**

Here is an example of the request. 

```json
PATCH https://{businesscentralPrefix}/api/v2.0/companies(companyId)/items(itemId)/picture(itemId)/content
```

**Response**

No response. 

## See also
[Tips for working with the APIs](../../../developer/devenv-connect-apps-tips.md)    
[picture](../resources/dynamics_picture.md)    
[Get picture](dynamics_picture_Get.md)    
[Delete picture](dynamics_picture_Delete.md)    
