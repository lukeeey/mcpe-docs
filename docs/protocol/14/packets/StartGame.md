---
permalink: /protocol/14/packets/start-game/
---
## Start Game

| Client Name     | Packet ID | Sent from Client | Sent from Server |
| --------------- | --------- | ---------------- | ---------------- |
| StartGamePacket | 0x87      | No               | Yes              |

---

### Fields

| Field     | Type | Description           |
| --------  | ---- | --------------------- |
| Seed      | int  | The seed of the world |
| Generator | int  | |
| Gamemode  | int  | • 0 - Survival <br> • 1 - Creative |
| Entity ID | int  | |
| X         | float  | The X coordinate of the player |
| Y         | float  | The Y coordinate of the player |
| Z         | float  | The Z coordinate of the player |
