---
permalink: "/rest-api/realms/replace-world-with-backup/"
---

## Replace World With Backup
This endpoint replaces the world with the specified backup.

| Host                        | Authentication |
| --------------------------- | -------------- |
| pocket.realms.minecraft.net | XBL 3.0        |

---

### Constructing the request
```
PUT /worlds/{id}/backups?backupId={backupId}
```

**{id}** is the specific id of the realm.  
**{backupId}** is the specified id of the backup. You can get it by [listing backups](../list-backups).  

Headers  
* `Authorization: {token}`    - **{token}** is your xbox live token  
* `Client-Version: {version}` - **{version}** is the version of the client
* `User-Agent: {agent}`       - **{agent}** is one of [these](../../#user-agents)

<br>

### Response
I'm not sure what the success response is yet. I need a non expired realm to test.  
<br>
If the realm has expired, the server will return
```json
{
    "errorCode": 403,
    "errorMsg": "No valid subscription"
}
```
