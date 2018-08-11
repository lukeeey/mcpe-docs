---
permalink: /rest-api/misc/featured-servers/
---
## Featured Servers
This endpoint returns information about the Microsoft supported featured servers that nobody likes.

| Host                        | Authentication |
| --------------------------- | -------------- |
| xforge.xboxlive.com         | XBL 3.0        |

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
        "filterQuery": "contentType eq '3PP'and platforms/any(p: p eq 'uwp.store')",
        "scids": [
            "4fc10100-5f7a-4470-899b-280835760c07"
        ]
    },
    "orderBy": {
        "direction": "DESC",
        "field": "creationDate"
    },
    "top": 25
}
```

<br>

Once you have done that, you should get a response like the following example which has been stripped down to save space (at the time of writing there is 4 featured servers in the `results` array below, and the `count` was originally 4)  

```json
{
    "count": 1,
    "results": [
        {
            "score": 1.0,
            "document": {
                "productId": "G009SXK64ZMT",
                "title": "CubeCraft Games",
                "description": "Lobby Description...",
                "contentType": "3PP",
                "scids": [
                    "4fc10100-5f7a-4470-899b-280835760c07"
                ],
                "platforms": [
                    "android.amazonappstore",
                    "android.googleplay",
                    "appletv.store",
                    "ios.store",
                    "oculus.store.rift",
                    "oculus.store.gearvr",
                    "uwp.store",
                    "uwp.store.mobile",
                    "xboxone.store"
                ],
                "tags": [
                    "G009SXK64ZMT"
                ],
                "visibility": "Public",
                "creatorId": "2535444456665343",
                "creatorGamertag": "CubeCraftGames",
                "thumbnailUrl": "https://ugcorigin.s-microsoft.com/15/58896f65-2e94-4ddb-b2bd-2f7aa2cffa5e/580/XboxThumbnail.jpg",
                "creationDate": "2017-07-26T16:50:02.442+00:00",
                "lastModifiedDate": "2018-08-09T17:00:00.264+00:00",
                "custom": {
                    "creatorName": "CubeCraft",
                    "minClientVersion": "1.2.13",
                    "port": 19132,
                    "requireXBL": true,
                    "url": "mco.cubecraft.net",
                    "whitelistUrl": "*.cubecraft.net"
                }
            }
        }
    ]
}
```

* `productId` is the resource id of the specified featured server content. You can use this if you want to get info for the specific server by making a **GET** request to **https://xforge.xboxlive.com/v1/catalog/items/{productId}**  
* `title` is the title displayed on the server list  
* `description` doesnt seem to do much, since the server motd is returned via normal query  
* `thumbnailUrl` is the server icon which is displayed on the serer list  
* `creatorName` is the name of the server creator (generally the company name, such as Mineplex LLC)  
* `minClientVersion` is the minimum client version required to join the server *(yes, these servers support multiple versions)*  
* `port` is the port of the server  
* `requireXBL` returns **true** if the server forces xbox live authentication, **false** if not  
* `url` is the address of the server. You can add this (along with the port above) just like a normal server if you wanted  
