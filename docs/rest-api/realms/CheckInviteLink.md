---
permalink: /rest-api/realms/check-invite-link/
---
## Check Invite Link
This endpoints checks the specified invite link for existance and if so, returns the realm info associated with the link.

| Host                        | Authentication |
| --------------------------- | -------------- |
| pocket.realms.minecraft.net | XBL 3.0        |

---

### Constructing the requests
```
GET /worlds/v1/link/{id}
```

**{id}** is the id of the link

Headers  
* `Authorization: {token}`    - **{token}** is your xbox live token  
* `Client-Version: {version}` - **{version}** is the version of the client
* `User-Agent: {agent}`       - **{agent}** is one of [these](../../#user-agents)

<br>

### Response
If the link id provided is invalid, the server will return
```json
{
    "errorCode": 403,
    "errorMsg": "Invalid link"
}
```

If the link however is valid, the server will return [the realm info](../realm-info/).
