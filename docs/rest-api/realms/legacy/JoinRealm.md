---
permalink: /rest-api/realms/legacy/join-realm/
---
## Join Realm
This endpoint returns the actual address and port of the realms server, as well as the encryption key. The client then connects to that address.

| Host                        | Authentication |
| --------------------------- | -------------- |
| peoapi.minecraft.net        | ?              |

---

### Constructing the request
```
POST /server/{id}/join
```

**{id}** is the specific id of the realm.  

<br>

### Response
Example Response
```json
{
   "ip": "87.169.167.12",
   "port": 21647,
   "key": "/6UAOMG6Q/EIjHxLa87un5l=="
}
```

* `ip` - The IP address of the actual remote server  
* `port` - The port of the actual remote server  
* `key` - The key used to encrypt the data received on the server (AES-128 ECB)
