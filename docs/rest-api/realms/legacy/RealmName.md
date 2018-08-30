---
permalink: /rest-api/realms/legacy/realm-name/
---
## Realm Name
This endpoints changes the name of the realm to the specified one. 

| Host                        | Authentication |
| --------------------------- | -------------- |
| peoapi.minecraft.net        | ?              |

---

### Constructing the request
```
PUT /server/{id}/name/{name}
```

* **{id}** is the id of the realm *(from [List Realms](../list-realms/))*  
* **{name}** is the name to change the current realm name to  

<br>

### Response
There is no response.