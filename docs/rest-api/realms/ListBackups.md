---
permalink: /rest-api/realms/list-backups/
---
## List Backups
This endpoint returns all the backups of the specified realm that have been made.

| Host                        | Authentication |
| --------------------------- | -------------- |
| pocket.realms.minecraft.net | XBL 3.0        |

---

### Constructing the request
```
PUT /worlds/{id}/backups
```

**{id}** is the specific id of the realm.   

Headers  
* `Authorization: {token}`    - **{token}** is your xbox live token  
* `Client-Version: {version}` - **{version}** is the version of the client
* `User-Agent: {agent}`       - **{agent}** is one of [these](../#user-agents)

<br>

### Response
If any backups exist, the server will return an array with each backup. You can loop through these.  
<br>
Example Response
```json
{
    "backups": [
        {
            "backupId": "ogNOWtdZyKfaJvwO4SS7nt3JzOVOQ2HW",
            "lastModifiedDate": 1523827627000,
            "size": 1648576,
            "metadata": {
                "game_difficulty" :"1",
                "name": "lukeeey21's Realm",
                "description": "",
                "game_mode": "0",
                "world_type": "NORMAL"
            }
        }
    ]
}
```

I havent tested but i assume if there are no backups then it will return
```json
{
    "backups": []
}
```
