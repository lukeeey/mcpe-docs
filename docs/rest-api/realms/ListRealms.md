---
permalink: /rest-api/realms/list-worlds/
---
## List Realms
This endpoint returns all the realms that you are a part of.

| Host                        | Authentication |
| --------------------------- | -------------- |
| pocket.realms.minecraft.net | XBL 3.0        |

---

### Constructing the request
```
GET /worlds
```

Headers  
* `Authorization: {token}`    - **{token}** is your xbox live token  
* `Client-Version: {version}` - **{version}** is the version of the client
* `User-Agent: {agent}`       - **{agent}** is one of [these](../#user-agents)

<br>

### Response
Once you have done that, you should get a response like the following example which has been stripped down to save space (just remember to loop through the `servers` array).    

```json
{
    "servers": [
        {
            "id": 1800696,
            "remoteSubscriptionId": "21d5f30194434e40b42bfa91dd7cd22c",
            "owner": "",
            "ownerUUID": "2535459632708673",
            "name": "lukeeey21's Realm",
            "motd": "",
            "state": "OPEN",
            "daysLeft": -1,
            "expired": true,
            "expiredTrial": false,
            "gracePeriod": false,
            "worldType": "NORMAL",
            "players": null,
            "maxPlayers": 10,
            "minigameName": null,
            "minigameId": null,
            "minigameImage": null,
            "activeSlot": 1,
            "slots": null,
            "member": false,
            "clubId": 3379870294579661
        }
    ]
}
```

* `id` is the unique id of the realm **(keep this as you will need it later)**  
* `ownerUUID` is the xbox live uuid of the realm owner  
* `name` is the realm name to be displayed on the realm list  
* `state` is either **OPEN** or **CLOSED**  
* `daysLeft` is an integer detailing how many days the realm has left before it expires. I think -1 means it has expired, not sure  
* `expired` returns **true** if the realm has expired, **false** if not  
* `maxPlayers` is the maximum amount of players allowed to join the realm at once, presumably always 10  

<br>

Once you have got the id of the realm you want to get more info about, you have a few options:  

* Return [more detailed info](../world-info/) on that realm  
* [Open](../open-world/) the realm  
* [Close](../close-world/) the realm  