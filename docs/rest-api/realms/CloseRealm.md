---
permalink: /rest-api/realms/close-realm/
---
## Close Realm
This endpoint essentially turns off the realm so that nobody can join it.

| Host                        | Authentication |
| --------------------------- | -------------- |
| pocket.realms.minecraft.net | XBL 3.0        |

---

### Constructing the request
```
PUT /worlds/{id}/close
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
