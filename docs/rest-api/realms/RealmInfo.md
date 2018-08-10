---
permalink: /rest-api/realms/world-info/
---
## Realm Info
This endpoint returns more detailed info about the specified realm.

| Host                        | Authentication |
| --------------------------- | -------------- |
| pocket.realms.minecraft.net | XBL 3.0        |

---

### Constructing the request
```
GET /worlds/{id}
```

**{id}** is the specific id of the realm which you can get by [listing worlds](../list-worlds/).

Headers  
* `Authorization: {token}`    - **{token}** is your xbox live token  
* `Client-Version: {version}` - **{version}** is the version of the client
* `User-Agent: {agent}`       - **{agent}** is one of [these](../#user-agents)

<br>

### Response
If the specified world exists and you are the owner, the server will return something like this
```json
{  
    "id": 1800696,
    "remoteSubscriptionId": "21d5f30194434e40b42bfa91dd7cd22c",
    "owner": null,
    "ownerUUID": "2535459632708673",
    "name": "lukeeey21's Realm",
    "motd": "",
    "state": "OPEN",
    "daysLeft": 29,
    "expired": false,
    "expiredTrial": false,
    "gracePeriod": false,
    "worldType": "NORMAL",
    "players": [  
        {  
            "uuid": "2535411257928271",
            "name": null,
            "operator": false,
            "accepted": true,
            "online": false
        }
    ],
    "maxPlayers": 10,
    "minigameName": null,
    "minigameId": null,
    "minigameImage": null,
    "activeSlot": 1,
    "slots": [  
        {  
            "options":"{\"slotName\":null,\"pvp\":true,\"spawnAnimals\":true,\"spawnMonsters\":true,\"spawnNPCs\":true,\"spawnProtection\":0,\"commandBlocks\":false,\"forceGameMode\":false,\"gameMode\":0,\"difficulty\":1,\"worldTemplateId\":-1,\"worldTemplateImage\":null,\"adventureMap\":false,\"resourcePackHash\":null,\"versionRef\":\"397f8b1a7cbc3ebca78178175b21123bd7b74afe\",\"versionLock\":false,\"cheatsAllowed\":true,\"texturePacksRequired\":false,\"enabledPacks\":{\"resourcePacks\":[],\"behaviorPacks\":[]},\"availablePacks\":{\"resourcePacks\":[],\"behaviorPacks\":[]}}",
            "slotId": 1
        }
    ],
    "clubId": 3379870294579661,
    "member": false
}
```

If you are *not* the owner, it will return
```json
{
	"errorCode": 403,
	"errorMsg": "Not owner"
}
```