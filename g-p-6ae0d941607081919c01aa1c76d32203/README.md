# Arena Surge

A runnable 3D browser multiplayer battle-arena prototype. It has WASD movement, mouse camera/aim, client raycast shooting with server-side range/angle validation, health, scoring, three-second respawns, and WebSocket multiplayer presence.

## Local run

1. Install Node.js 18+.
2. From this project folder, run `npm start`.
3. Open `http://localhost:3000` in two browser tabs. Enter different names and use each tab to move/aim/shoot.

The browser imports Three.js from unpkg, so the browser needs internet access on its first load. The Node server has no package-install dependency.

## Deployment

Deploy to any host that supports a long-lived Node process and WebSockets. Set the start command to `npm start`; the service automatically reads the host-provided `PORT`. Use HTTPS in production so browsers connect through `wss` automatically.

## Prototype limitations

This is intentionally a starter, not a zero-defect or cheat-proof game. Movement is client-reported and the server validates only bounds plus shot range/angle; production should add authoritative physics, authentication, rate limits, reconnection, persistence, monitoring, and automated multi-client/browser tests.