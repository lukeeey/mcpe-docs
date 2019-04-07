---
permalink: "/rest-api/realms/pending-invites-count/"
---

## Pending Invites Count
This endpoint returns the amount of players who have been invited to your realm but have not responded to the invite.

| Host                        | Authentication |
| --------------------------- | -------------- |
| pocket.realms.minecraft.net | XBL 3.0        |

---

### Constructing the request
```
GET /invites/count/pending
```

Headers  
* `Authorization: {token}`    - **{token}** is your xbox live token  
* `Client-Version: {version}` - **{version}** is the version of the client
* `User-Agent: {agent}`       - **{agent}** is one of [these](../../#user-agents)

<br>

### Response
The response will be an integer. I have not invited any players to my realm so it returns `0`.
