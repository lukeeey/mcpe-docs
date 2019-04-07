---
permalink: "/rest-api/realms/legacy/create-realm/"
---

## Create Realm
This endpoint creates the realm.

| Host                        | Authentication |
| --------------------------- | -------------- |
| peoapi.minecraft.net        | ?              |

---

### Constructing the request
```
POST /server/create?name={name}&type={type}&seed={seed}
```

* **{name}** is the title of the server  
* **{type}** is the game mode of the server. Can be either `creative` or `survival`  
* **{seed}** is the seed for the world  

<br>

### Response
Not sure if there even is a response.