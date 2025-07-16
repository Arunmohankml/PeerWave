---

# PeerWave (PW) - Simple Voice Chat API
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![PeerJS](https://img.shields.io/badge/PeerJS-0099ff?style=for-the-badge&logo=webrtc&logoColor=white)
![WebRTC](https://img.shields.io/badge/WebRTC-333333?style=for-the-badge&logo=webrtc&logoColor=white)
![Glitch](https://img.shields.io/badge/Glitch-5C2D91?style=for-the-badge&logo=glitch&logoColor=white)
![Acode](https://img.shields.io/badge/Acode-Mobile%20IDE-2C2C2C?style=for-the-badge&logo=android&logoColor=green)

**PeerWave** is a lightweight, plug-and-play voice communication API for web apps, built using [PeerJS](https://peerjs.com/). This library allows you to integrate real-time voice chat between users with just a few function calls. This can be mainly used for proximity making proximity/normal voicechat in games with inbuilt browser or normal Websites.

- currently it's using peerjs default cloud server for signaling, it may cause minor bugs, feel free to contribute and upgrade these features.

Hosted Library:  
🔗 [https://arunmohankml.github.io/PeerWave-server/voice.js](https://arunmohankml.github.io/PeerWave-server/voice.js)
---
### Features

- Connect to voice
- Call player
- Control call volume
- Control self volume
- Mute/unmute

---

## 🔧 How to Use

### 1. Include PeerWave and Peerjs in Your HTML

```
<script src="https://unpkg.com/peerjs@1.5.5/dist/peerjs.min.js"></script>
<script src="https://stump-deadpan-wall.glitch.me/voice.js"></script>
```

---

📚 API Reference

```PW.connectToVoice(peerId: string)```

Initializes the connection to the PeerJS server and sets up your microphone.

peerId: A unique string that identifies your client.


Example:

`PW.connectToVoice("player123");`


---

```PW.callUser(targetPeerId: string)```

Initiates a call to another peer.

targetPeerId: The ID of the peer you want to call.


Example:

`PW.callUser("player456");`


---

```PW.setUserVolume(peerId: string, volume: number)```

Controls the volume of a specific connected peer.

peerId: The ID of the peer whose volume you want to adjust.

volume: A number from 0.0 (mute) to 1.0 (full volume).


Example:

`PW.setUserVolume("player456", 0.5); // Set volume to 50%`


---

```PW.setMyVolume(volume: number)```

Adjusts the outgoing microphone volume.

volume: A number from 0.0 (mute) to 1.0 (full volume).


Example:

`PW.setMyVolume(0.0); // Mute yourself
`
This is useful for implementing push-to-talk functionality.


---

```PW.getConnectedUsers():``` Array

Returns a list of all currently connected peers.

Example:

`const users = PW.getConnectedUsers();
console.log(users);`

Each item in the array has:

`{
  peer_id: "targetPeerId",
  call: PeerMediaConnection
}`


---

Example HTML Template

You can find a working client implementation with UI at:
🔗 [PREVIEW](https://arunmohankml.github.io/PeerWave/)


---

Credits

This library is created and maintained by [Arunmohankml](https://github.com/Arunmohankml/j).
Please give proper credit if you use or modify this library in your projects.


---
