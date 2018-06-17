---
permalink: /rest-api/realms/join-realm/
---
## Join Realm
This endpoint returns the actual address and port of the realms server. The client then connects to that address.

| Host                        | Authentication |
| --------------------------- | -------------- |
| pocket.realms.minecraft.net | XBL 3.0        |

---

### Constructing the request
```
GET /worlds/{id}/join
```

**{id}** is the specific id of the realm.

Headers  
* `Authorization: {token}`    - **{token}** is your xbox live token  
* `Client-Version: {version}` - **{version}** is the version of the client
* `User-Agent: {agent}`       - **{agent}** is one of [these](../#user-agents)

<br>

### Response
If the realm has expired, the server will return
```json
{
    "errorCode": 403,
    "errorMsg": "No valid subscription"
}
```

And if its not, then it will return something like
```json
{
    "address": "ec2-34-245-144-180.eu-west-1.compute.amazonaws.com:27159",
    "pendingUpdate": false
}
```

The address is in the format `ip:port`. I'm not quite sure what `pendingUpdate` means.  

If you try to join using that address in the server list, beware the ip and port changes a lot and you can only join if you are invited to the realm.
