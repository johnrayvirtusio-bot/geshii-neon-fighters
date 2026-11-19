# Geshii: Neon Fighters

A small, playable 1v1 fighting-game prototype with a neon arena, keyboard and touch controls, and a solo training-bot mode. It runs in modern browsers and is configured to package as an Android app with Capacitor.

> **Prototype note:** PvP currently means local play on one device. Online matchmaking and network multiplayer are not implemented yet; they need a server/backend and are a separate feature.

## Play in a browser

Requirements: Node.js 18 or newer.

```bash
npm install
npm run dev
```

Open the local URL Vite prints (usually `http://localhost:5173`). To create a production build, run `npm run build`; the static site will be in `dist/`.

## Controls

- **Player 1:** `A` / `D` move, `W` jump, `F` jab, `G` heavy attack, `S` block.
- **Player 2:** `←` / `→` move, `↑` jump, `K` jab, `L` heavy attack, `↓` block.
- On phones, use the on-screen Player 1 controls. For best results, play in landscape.
- Choose **Solo Challenge** to fight the training bot.

## Android package

Install the Android SDK and Java/Android Studio, then:

```bash
npm install
npm run android:add
npm run android:sync
npm run android:open
```

Build and run the Android project from Android Studio. `android:add` is a one-time step; use `npm run android:sync` for later web changes.

## Current features

- Canvas-drawn neon arena and fighters
- Health, timer, round wins, hit sparks, blocking, jumping, and light/heavy attacks
- Local two-player and simple CPU modes
- Responsive touch controls and an offline-capable web app shell
- Capacitor Android configuration

## Next step for real online PvP

Online play requires an authoritative multiplayer service for matchmaking, rooms, player input synchronization, and reconnect handling. This repository deliberately labels local play accurately rather than suggesting the prototype already has online PvP.
