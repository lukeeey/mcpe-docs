---
permalink: "/protocol/14/login-status/"
---

## Login Status

| Client Name        | Packet ID | Sent from Client | Sent from Server |
| ------------------ | --------- | ---------------- | ---------------- |
| LoginStatusPacket  | 0x83      | No               | Yes              |

---

### Fields

| Field  | Type | Description                                                                                       |
| ------ | ---- | ------------------------------------------------------------------------------------------------- |
| Status | int  | • 0 - Login Success <br> • 1 - Server Outdated <br> • 2 - Client Outdated <br> • 3 - Player Spawn |

If the login was successful, you need to send a [StartGamePacket](../start-game/).
