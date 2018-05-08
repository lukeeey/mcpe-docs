---
permalink: /rest-api/realms/legacy/status/
---
## Join Realm
This endpoint returns whether or not server creation is allowed.

| Host                        | Authentication |
| --------------------------- | -------------- |
| peoapi.minecraft.net        | ?              |

---

### Constructing the request
```
GET /info/status
```


### Response
Example Response
```json
{
    "serviceEnabled": true,
    "buyServerEnabled": false,
    "createServerEnabled": false
}
```

* `serviceEnabled` - Whether the realms service is enabled?  
* `buyServerEnabled` -  Whether server buying is enabled?
* `createServerEnabled` - Whether server creation is enabled?
