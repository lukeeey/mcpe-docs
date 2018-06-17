---
permalink: /rest-api/realms/client-compatible/
---
## Client Compatible
This endpoint returns whether or not the client version is compatible with realms.

| Host                        | Authentication |
| --------------------------- | -------------- |
| pocket.realms.minecraft.net | XBL 3.0        |

---

### Constructing the request
```
GET /mco/client/compatible
```

Headers  
* `Authorization: {token}`    - **{token}** is your xbox live token  
* `Client-Version: {version}` - **{version}** is the version of the client
* `User-Agent: {agent}`       - **{agent}** is one of [these](../../#user-agents) 

<br>

### Response
If the client version is **not** compatible with realms, the server will return
```
OUTDATED
```

And if the client **is** compatible, it will return
```
COMPATIBLE
```
