---
permalink: /url-scheme/
---
## Minecraft Url Scheme
Minecraft: Bedrock Edition on Android and Windows 10 (not sure about other platforms) registers a custom url scheme. This means that you can launch the
app from a web browser, but it also means you can do a few other cool things :)

The only downside is that you cannot enter these directly into the address bar, they need to be a link on a website or a bookmark. You also can't click the links from Github.  

---

#### Launching Education Edition
Yes, you read it right. You can launch Minecraft: Education Edition from a browser. It works on Android too!

Link - [`minecraft:?edu=1`](minecraft:?edu=1)  

<br><br>

#### Add an External Server
For all you server owners out there, you can add an external server from a link. The format is `name|ip:port`, so for LBSG:

Link - [`minecraft:?addExternalServer=Lifeboat|sg.lbsg.net:19132`](minecraft:?addExternalServer=Lifeboat\|sg.lbsg.net:19132)  

<br><br>

#### Show Store on Startup
This link will open Minecraft and, instead of showing the home screen, immediatly open the store screen.

Link - [`minecraft:?showStoreHomeScreen=1`](minecraft:?showStoreHomeScreen=1)   

It seems that `showStoreOffer` is also the same as `showStoreHomeScreen`, so you could use that if you wanted.  

<br><br>

#### Accept Realms Invite
There are actually 2 ways to accept a realms invite from the browser. The first one actually uses the second method but it has a pretty interface.

**Method 1**  
Visit https://open.minecraft.net/pocket/realms/invite/{id}, where **{id}** is the realms invite code. For example: `lpomEvbo88E` is mine at the time of writing.  

**Method 2**  
If you want to completely skip the interface, just use `minecraft://acceptRealmInvite?inviteID={id}`
