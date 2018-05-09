---
permalink: /protocol/14/
---
## Protocol 14

| Number of Packets | RakNet Protocol Version | Client Version |
| ----------------- | ----------------------- | -------------- |
| 52                | 5                       | 0.8.1, 0.9.0   |

Mojang made an error in 0.9.0 build 1 which kept the protocol at `14`. This was fixed in build 2.

---

#### Packet List

| Packet Name                   | Packet ID |     
| ----------------------------- | --------- |  
| [Login](login/)               | 0x82      |     
| [Login Status](login-status/) | 0x83      |     
| [Ready](ready/)               | 0x84      |    
| Message                       | 0x85      |     
| [Set Time](set-time/)         | 0x86      |     
| [Start Game](start-game/)     | 0x87      |     
| [Add Mob](add-mob/)           | 0x88      |     
| Add Player                    | 0x89      |     
| Remove Player                 | 0x8a      |     
| Add Entity                    | 0x8c      |     
| Remove Entity                 | 0x8d      |     
| Add Item Entity               | 0x8e      |     
| Take Item Entity              | 0x8f      |     
| Move Entity                   | 0x90      |     
| Move Entity PosRot            | 0x93      |     
| Rotate Head                   | 0x94      |     
| Move Player                   | 0x95      |     
| Place Block                   | 0x96      |     
| Remove Block                  | 0x97      |     
| Update Block                  | 0x98      |     
| Add Painting                  | 0x99      |     
| Explode                       | 0x9a      |     
| Level Event                   | 0x9b      |     
| Tile Event                    | 0x9c      |     
| Entity Event                  | 0x9d      |     
| Request Chunk                 | 0x9e      |     
| Chunk Data                    | 0x9f      |     
| Player Equipment              | 0xa0      |     
| Player Armor Equipment        | 0xa1      |     
| Interact                      | 0xa2      |     
| Use Item                      | 0xa3      |     
| Player Action                 | 0xa4      |     
| Hurt Armor                    | 0xa6      |     
| Set Entity Data               | 0xa7      |     
| Set Entity Motion             | 0xa8      |     
| Set Entity Link               | 0xa9      |     
| Set Health                    | 0xaa      |     
| Set Spawn Position            | 0xab      |     
| Animate                       | 0xac      |     
| Respawn                       | 0xad      |     
| Send Inventory                | 0xae      |     
| Drop Item                     | 0xaf      |     
| Container Open                | 0xb0      |     
| Container Close               | 0xb1      |     
| Container Set Slot            | 0xb2      |     
| Container Set Data            | 0xb3      |     
| Container Set Content         | 0xb4      |     
| Container ACK                 | 0xb5      |     
| Chat                          | 0xb6      |     
| Adventure Settings            | 0xb7      |     
| Entity Data                   | 0xb8      |     
| Player Input                  | 0xb9      |     
