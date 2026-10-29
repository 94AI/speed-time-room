# 倍速時光屋｜影音加速器 — Fork Notes

Independent per-player edition of Video Speed Controller, based on official v0.11.1, commit `8f9bc13cd1d8bad549795da265735159d9e9fad1`. MIT license and upstream attribution are retained. This independent distribution does not modify the upstream repository.

Public version 0.11.3 (`0.11.3-zh-TW.1`) matches the runtime submitted to the Chrome Web Store on 2026-10-28. It removes raw keyboard-event diagnostic logging, points fork feedback to 94AI/speed-time-room, and documents local data handling. The full unit/integration suite passed 546 tests across 44 files. Store approval is pending as last checked on 2026-10-28.

Each video/audio element owns its chosen speed. Peer actions, native holds, resource initialization and lifecycle restoration cannot replace that target with another player's speed. Global remembered-speed propagation is disabled. Explicit site defaults remain available. Custom shortcuts and controller CSS/position/opacity/buttons are preserved. The new Mac-style logo is included separately and at Chrome icon sizes.

Build: Node.js 22.22.2+, 24.15.0+, or 26+; `npm ci`, `npm test`, `npm run lint`, `npm run build`. Load `dist/` through Chrome's Developer mode / Load unpacked. Browser regression: `npm run test:e2e:private` (requires Puppeteer's downloaded Chrome; `CHROME_PATH` can select a compatible testing browser).

See `docs/speed-arbitration.md` for the per-player architecture. The shipped Traditional Chinese installation guide and verification report explain targeting, installation, compatibility limits, and what was actually executed.
