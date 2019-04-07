---
permalink: "/protocol/14/set-time/"
---

## Set Time

| Client Name    | Packet ID | Sent from Client | Sent from Server |
| -------------- | --------- | ---------------- | ---------------- |
| SetTimePacket  | 0x86      | No               | Yes              |

---

### Fields

| Field   | Type | Description                                 | 
| ------- | ---- | ------------------------------------------- |
| Time    | int  | The time of the world                       |
| Started | byte | • 0x80 - Start Time <br> • 0x00 - Stop Time |
