# Peloponnesian Front 3D (mobile-first prototype)

This is a third-person 3D browser prototype with real-time multiplayer networking.

## Included
- Three.js third-person 3D battlefield and stylised hoplite soldiers
- Athens and Sparta teams, up to 30 players per side (60 total)
- Mobile touch movement/look controls and desktop WASD
- Directional attack buttons, held shield guard, sprint
- Weapon selection: spear, xiphos, kopis, bow (prototype moveset/damage differences)
- Server-side team capacity, health, stamina, hits and respawn
- Render deployment blueprint

## Deploy online with a shareable link (Render)

You need a GitHub account and a Render account. The accounts may have free options; hosting limits/prices can change. This project is not deployed yet and has no live public URL.

1. Download and unzip this project.
2. Create a GitHub repository, for example `peloponnesian-front-3d`.
3. Upload the *contents* of the unzipped folder (not the ZIP itself) to the repository.
   - On GitHub: repository -> Add file -> Upload files -> drag in `server.js`, `package.json`, `index.html`, `client.js`, `style.css`, and `render.yaml`.
4. Sign in at https://render.com/
5. In Render choose **New +** -> **Blueprint**.
6. Connect GitHub and select your `peloponnesian-front-3d` repository.
7. Render detects `render.yaml`. Review and create/deploy the service.
8. Wait for deployment to finish. Render displays a URL ending in `onrender.com`.
9. Open that URL on your phone. Send the exact same URL to friends. Everyone joins the same live server.
10. For best phone controls, rotate to landscape and use Chrome.

If Render's Blueprint option is unavailable, create **New + -> Web Service**, select the repository, choose Node as runtime, set build command `npm install` and start command `npm start`. No database is required for this prototype.

## Test locally
Install Node.js 18+, then in this folder:
```bash
npm install
npm start
```
Open http://localhost:3000. For friends on other networks, deploy it online; localhost is only your own device.

## Honest prototype limits
This is an early 3D prototype, not a finished commercial game. It uses simple stylised low-poly soldiers, a small arena, simplified hit detection and basic directional guard. Attack direction buttons currently select attack types; they are not a full animation-driven directional sword-fighting simulation. The bow is a short-range prototype hit check, not a projectile system. Weapon switching is a prototype feature, not a historically balanced progression system.

The server enforces a maximum of 30 per team, but it has not been load-tested with 60 concurrent players. Free hosting can sleep, throttle resources or change its terms. Test with a few friends first, then scale hosting only if needed. This is a browser game; no native Android APK is included.
