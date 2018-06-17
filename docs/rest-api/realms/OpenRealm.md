---
permalink: /rest-api/realms/open-realm/
---
## Open Realm
This endpoint turns the realm back on, allowing players to join.

| Host                        | Authentication |
| --------------------------- | -------------- |
| pocket.realms.minecraft.net | XBL 3.0        |

---

### Constructing the request
```
PUT /worlds/{id}/open
```

**{id}** is the specific id of the realm.

Headers  
* `Authorization: {token}`    - **{token}** is your xbox live token  
* `Client-Version: {version}` - **{version}** is the version of the client
* `User-Agent: {agent}`       - **{agent}** is one of [these](../../#user-agents)

<br>

### Response
If successful, the server will simply return
```
true
```
