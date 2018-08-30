---
permalink: /rest-api/realms/legacy/close-realm/
---
## Close Realm
This endpoints makes the realm offline so nobody can join.

| Host                        | Authentication |
| --------------------------- | -------------- |
| peoapi.minecraft.net        | ?              |

---

### Constructing the request
```
PUT /server/{id}/close
```

* **{id}** is the id of the realm *(from [List Realms](../list-realms/))*  

<br>

### Response
There is no response.