---
permalink: /rest-api/realms/legacy/list-realms/
---
## List Realms
This endpoint lists all realms that the user owns or has been invited to.  

| Host                        | Authentication |
| --------------------------- | -------------- |
| peoapi.minecraft.net        | ?              |

---

### Constructing the request
```
GET /server/list
```


### Response
Example Response (not sure about this, response from wiki.vg)  
```json
[
    {
        "serverId": 1,
        "name": "lukeeey21's Server",
        "open": true,
        "ownerName": "lukeeey21",
        "myWorld": true,
        "maxNrPlayers": 10,
        "type": "survival",
        "playerNames": ["lukeeey21", "Dogle601", "williamtdr"],
        "invited": ["lukeeey21", "Dogle601", "williamtdr"],
        "daysLeft": 0
    }
]
```

* `serverId` is the id of the realm  
* `name` is the title of the server  
* `open` is `true` if joinable, `false` if not  
* `ownerName` is the username of the realm owner  
* `myWorld` returns `true` if the realm belongs to the current user  
* `maxNrPlayers` is the maximum amount of player allowed to join the realm  
* `type` is the server gamemode, `creative` or `survival`  
* `playerNames` is an array of player usernames who are currently on the server  
* `invited` is an array of player usernames who haved been invited to the server  
* `daysLeft` is the amount of days the realm has before it expires  