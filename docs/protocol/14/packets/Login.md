---
permalink: /protocol/14/packets/login/
---
## Login

| Client Name | Packet ID | Sent from Client | Sent from Server |
| ----------- | --------- | ---------------- | ---------------- |
| LoginPacket | 0x82      | Yes              | No               |

---

### Fields

| Field      | Type   | Description                 |
| ---------- | ------ | --------------------------- |
| Username   | string | The username of the player  |
| protocol1  | int    | |
| protocol2  | int    | |
| Client ID  | int    | The Client ID of the player |
| Login Data | string | |

