# find-the-number
A 2 player based game

How it connects:
- The first person to enter a room code becomes the host, and the second connects to them directly.
- No accounts or sign-in are needed. You just share the link and the code.

Things to know:
- Reloading drops the match. If the host reloads, their room code can stay reserved for a few seconds, so the other player may see a “couldn’t reach the room” message. Waiting a moment and reloading fixes it.
- Strict networks can block the connection. Some mobile carriers and corporate networks stop WebRTC from connecting directly, and you’d need a TURN server to get past that. Home Wi-Fi to home Wi-Fi is usually fine.
- The signaling server is community-run. PeerJS’s free default server is maintained by volunteers. For something you plan to keep long-term, you can run your own PeerServer and point new Peer(...) at it, which is a small change.
