---
permalink: /rest-api/realms/get-invite-link/
---
## Get Invite Link
This endpoint returns the invite link for a realm.

| Host                        | Authentication |
| --------------------------- | -------------- |
| pocket.realms.minecraft.net | XBL 3.0        |

---

### Constructing the requests
```
GET /links/v1?worldId={id}
```

**{id}** is the specific id of the realm.

Headers  
* `Authorization: {token}`    - **{token}** is your xbox live token  
* `Client-Version: {version}` - **{version}** is the version of the client
* `User-Agent: {agent}`       - **{agent}** is one of [these](../#user-agents)

<br>

### Response
Example Response
```json
[
    {
        "linkId": "lpomEvbo88E",
        "profileUuid": "2535459632708673",
        "type": "INFINITE",
        "ts": 1523271890155,
        "url": "https://realms.gg/lpomEvbo88E",
        "deepLinkUrl": "minecraft://acceptRealmInvite?inviteID=lpomEvbo88E"
    }
]
```

* `linkId` is the invite link you were looking for  
* `type` is the world type of the realm  
* `url` is the web link to join your realm  
* `deepLinkUrl` is the direct link which opens Minecraft and accepts the invite  
