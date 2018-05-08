---
permalink: /protocol/14/packets/login-status/
---
## Login Status

| Client Name        | Packet ID | Sent from Client | Sent from Server |
| ------------------ | --------- | ---------------- | ---------------- |
| LoginStatusPacket  | 0x83      | No               | Yes              |

---

### Fields

| Field      | Type   | Description                 |
| ---------- | ------ | --------------------------- |
| Status     | int    | • 0 - Success <br> • 1 - Failed Client <br> * 2 - Failed Server <br> * 3 - Player Spawn |


