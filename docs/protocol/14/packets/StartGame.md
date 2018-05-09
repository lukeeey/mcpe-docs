---
permalink: /protocol/14/start-game/
---
## Start Game

| Client Name     | Packet ID | Sent from Client | Sent from Server |
| --------------- | --------- | ---------------- | ---------------- |
| StartGamePacket | 0x87      | No               | Yes              |

---

### Fields

| Field     | Type  | Description                                                                                          |
| --------- | ----- | ---------------------------------------------------------------------------------------------------- |
| Seed      | int   | The seed of the world, the client doesn't really care about this so you can set it to -1 if you want |
| Generator | int   |                                                                                                      |
| Gamemode  | int   | • 0 - Survival <br> • 1 - Creative                                                                   |
| Entity ID | int   |                                                                                                      |
| X         | float | The X coordinate of the player                                                                       |
| Y         | float | The Y coordinate of the player                                                                       |
| Z         | float | The Z coordinate of the player                                                                       |
