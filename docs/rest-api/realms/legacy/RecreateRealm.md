---
permalink: /rest-api/realms/legacy/recreate-realm/
---
## Rereate Realm
I think this endpoint recreates a world from an existing one? Like a fresh start.

| Host                        | Authentication |
| --------------------------- | -------------- |
| peoapi.minecraft.net        | ?              |

---

### Constructing the request
```
PUT /server/{id}/recreate?name={name}&type={type}&seed={seed}
```

* **{id}** is the id of the existing realm  
* **{name}** is the title of the server  
* **{type}** is the game mode of the server. Can be either `creative` or `survival`  
* **{seed}** is the seed for the world  

<br>

### Response
There is no response.