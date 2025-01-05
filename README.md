

# 2025_01_01_WsBeaconBroadcasterDDNS  

Leverage Python Tornado to host beacons that can receive and broadcast byte/text streams, enabling local users to connect. The aim is to build a scalable system capable of supporting up to 16,555 players receiving game data simultaneously.  

I want to create a game server where 16,555 players can engage in battle. This involves handling an immense amount of data flow. While the incoming data can be managed, the outgoing data requirements are staggering and pose a major challenge.  

For example, each player's position can be compressed to 12–16 bytes. Assuming 8 updates per second, that's 128 bytes per second per player. However, with 16,555 players, the data load for a single player to receive all updates becomes 2,119,040 bytes per second. Across all players, this adds up to an astronomical 32.7 GB per second of outgoing data. This far exceeds typical upload bandwidth, which ranges from 30 to 100 Mbps per broadcaster.  

Beyond game design considerations, I will need to develop a broadcasting system capable of scaling effectively. This will involve crafting code to distribute data via a dynamic DNS (DDNS) system and structuring beacons similar to an NTP network of interconnected computers.  

**Milestone A:** Allow Twitch Play players to receive information about the running game and remotely control their characters.    
**Milestone B:** Develop a small game that minimizes upload bandwidth usage using the concept.  
**Milestone C:** Gradually expand the game player size allowed and its features over time, growing month by month.    


> The code has not been started yet, but it is part of my 2025_01_01 resolution to enable the type of game I want to build.

> **Note:** To host a beacon, you need to know how to open ports and set up port forwarding.
