---
permalink: "/protocol/14/add-mob/"
---

## Add Mob

| Client Name  | Packet ID | Sent from Client | Sent from Server |
| ------------ | --------- | ---------------- | ---------------- |
| AddMobPacket | 0x86      | No               | Yes              |

---

### Fields

| Field       | Type  | Description           |
| ----------  | ----- | --------------------- |
| Entity ID   | int   | |
| Entity Type | int   | |
| X           | float | The X coordinate to spawn the mob |
| Y           | float | The Y coordinate to spawn the mob |
| Z           | float | The Z coordinate to spawn the mob |
| Yaw         | byte  | |
| Pitch       | byte  | |
| Metadata    | ?     | ? |
