---
permalink: /rest-api/misc/patch-notes/
---
## Patch Notes
This endpoint returns the patch notes for the specified client version. It requires 2 seperate requests to actually obtain the content.

| Host                        | Authentication |
| --------------------------- | -------------- |
| xforge.xboxlive.com         | XBL 3.0        |

There may not be patch notes available for every client version, so beware.  

---

### Making the requests
```
POST /v1/catalog/items/search
```

Headers  
* `Content-Type: application/json`  
* `Authorization: {xbox token}`  

<br>

Payload
```json
{
    "count": true,
    "filter": {
        "contentType": "PatchNotes",
        "platforms": [
            "minecraft"
        ],
        "tags": [
            "{clientVersion}"
        ],
        "titleId": "896928775"
    }
}
```

* `{clientVersion}` is the version of the client  

<br>

Once you have done that, you should get a response like the following example from 1.2.10:

```json
{
    "count": 1,
    "results": [
        {
            "score": 1.0,
            "document": {
                "productId": "G009SV5T6D3Z",
                "title": "1.2.10 Update!",
                "description": "",
                "contentType": "PatchNotes",
                "scids": [
                    "4fc10100-5f7a-4470-899b-280835760c07"
                ],
                "platforms": [
                    "minecraft"
                ],
                "tags": [
                    "1.2.10",
                    "1.2.10_development"
                ],
                "visibility": "Public",
                "creatorId": "2535448579972708",
                "creatorGamertag": "DampKeyboard157",
                "thumbnailUrl": "https://ugcorigin.s-microsoft.com/15/86f71573-562b-4aac-b296-bde3f800ec3b/580/XboxThumbnail.jpg",
                "creationDate": "2018-02-07T18:58:17.506+00:00",
                "lastModifiedDate": "2018-02-07T20:47:19.286+00:00",
                "custom": {
                    "minClientVersion": "1.2.10",
                    "offers": [
                        "G009SVF47JGW"
                    ],
                    "revision": "1.2.10.0"
                }
            }
        }
    ]
}
```

* `productId` is the resource id of the patch notes content, **you will need this, see below**  
* `title` is the title displayed in the patch notes screen  
* `creatorGamertag` is the xbox live gamertag of the content author. It’s usually *DampKeyboard157*. Not quite sure who that is  
* `thumbnailUrl` is the image which is displayed on the patch notes screen  
* `offers` is the offer to be displayed in the top right corner of the patch notes screen  

<br>

---

Now we can make the second request.

```
GET /v1/catalog/items/{productId}
```

* `{productId}` is the product id from the previous `POST` request you just made  

Headers
* `Content-Type: application/json`  

<br>

which returns something like

```json
{
    "id": "G009SV5T6D3Z",
    "title": {
        "neutral": "1.2.10 Update!"
    },
    "description": {
        "neutral": ""
    },
    "contentType": "PatchNotes",
    "scids": [
        "4fc10100-5f7a-4470-899b-280835760c07"
    ],
    "platforms": [
        "minecraft"
    ],
    "tags": [
        "1.2.10",
        "1.2.10_development"
    ],
    "sandbox": "RETAIL",
    "minimumClientVersion": "1.2.10",
    "creationDate": "2018-02-07T18:58:17.5067607+00:00",
    "lastModifiedDate": "2018-02-07T20:47:19.2869454+00:00",
    "startDate": "2017-10-04T15:00:00+00:00",
    "visibility": "Public",
    "contentUrls": [
        "https://ugcorigin.s-microsoft.com/15/1862ca1b-0000-0000-7a48-65058884e5f9/680/v2/mod.mod"
    ],
    "contents": [
        {
            "contentId": "1862ca1b-0000-0000-7a48-65058884e5f9",
            "contentType": "publicmod",
            "contentUri": "https://ugcorigin.s-microsoft.com/15/1862ca1b-0000-0000-7a48-65058884e5f9/680/v2/mod.mod"
        }
    ],
    "creatorId": "2535448579972708",
    "creatorGamertag": "DampKeyboard157",
    "images": [
        {
            "id": "86f71573-562b-4aac-b296-bde3f800ec3b",
            "uri": "https://ugcorigin.s-microsoft.com/15/86f71573-562b-4aac-b296-bde3f800ec3b/580/XboxThumbnail.jpg",
            "imagePurpose": "Thumbnail",
            "imageTag": "Thumbnail",
            "imageType": "Thumbnail",
            "height": -1,
            "width": -1
        }
    ],
    "custom": {
        "minClientVersion": "1.2.10",
        "offers": [
            "G009SVF47JGW"
        ],
        "revision": "1.2.10.0"
    }
}
```

Now we can get the compressed patch note files. In the JSON we just received, find the `contentUrls` array and download the file from the URL provided.  

If we were to use the above example, the URL would be [`https://ugcorigin.s-microsoft.com/15/1862ca1b-0000-0000-7a48-65058884e5f9/680/v2/mod.mod`](https://ugcorigin.s-microsoft.com/15/1862ca1b-0000-0000-7a48-65058884e5f9/680/v2/mod.mod).
Just visit the URL in a browser or download it programically :)   

The file downloaded is actually a compressed zip file, despite the exstension being .mod, so just **rename it to .zip** and open it.
