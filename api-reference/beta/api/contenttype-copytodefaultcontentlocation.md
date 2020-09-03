---
author: swapnil1993
ms.author: swapnil1993
title: "ContentType copyToDefaultContentLocation"
description: "Copy a file to default content location in a Content Type"
localization_priority: Normal
doc_type: apiPageType
ms.prod: "sharepoint"
---

# Copy a file to default content location in a Content Type
Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]
Copy a file to default content location in a [content type][contentType] so that they can be added as default content or template via POST operation.
  

## Permissions  

One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions_reference.md).

  

|Permission type | Permissions (from least to most privileged) |

|:--------------------|:---------------------------------------------------------|

|Delegated (work or school account) | Sites.ReadWrite.All, Sites.Manage.All, Sites.FullControl.All  |

|Delegated (personal Microsoft account) | Not supported. |

|Application | Sites.ReadWrite.All, Sites.Manage.All, Sites.FullControl.All |

  

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->

```http

POST https://graph.microsoft.com/v1.0/sites/id/contentTypes/id/copyToDefaultContentLocation 
```

## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|
|Content-Type|application/json. Required.|

## Request body
In the request body, supply JSON representation of the parameters.

The following table shows the parameters that can be used with this action.


|Parameter|Type|Required|Description|
|-|-|-|-|
|sourceFile| microsoft.graph.itemReference | Yes|Metadata about the source file that needs to be copied to the default content location.|
|destinationFileName| string | No|Destination filename . 

## Response


If successful, this call returns a `204 No Content` response

## Example

### Request
<!-- {
  "blockType": "request",
  "name": "contenttype_copytodefaultcontentlocation"
}
-->
```http
POST https://graph.microsoft.com/beta/sites/{id}/contentTypes/{contentTypeId}/copyToDefaultContentLocation 
Content-Type: application/json

{
	"sourceFile": {
		"sharepointIds": {
			"listId": "e2ecf63b-b0fd-48f7-a54a-d8c15479e3b0",
			"listItemId": "2"
		}
	},
	"destinationFileName": "newname.txt"
}
```



### Response


<!-- { "blockType": "response" } -->

```http
HTTP/1.1 204 No Content

```

  

[contentType]: ../resources/contentType.md