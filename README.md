# Friendsgiving Superlatives

A live superlatives game for parties. A TV or laptop runs the host screen, and guests vote from their phones by scanning a QR code. Guests don't need an app or an account, and it costs nothing to run.

It's a single file, `index.html`. The host screen acts as the game server. Phones connect straight to it through [PeerJS](https://github.com/peers/peerjs), an open-source library whose free public server only introduces the devices to each other.

## Put it online (free, about 5 minutes)

Phones need a web address to open, so the file has to be hosted somewhere. GitHub Pages is free:

1. Sign in at github.com and create a **new public repository**, for example `superlatives`.
2. Click **Add file → Upload files**, drag in `index.html`, then click **Commit changes**.
3. Go to **Settings → Pages**. Under "Branch", choose `main` and `/ (root)`, then click **Save**.
4. After a minute or two your game is live at `https://YOUR-USERNAME.github.io/superlatives/`.

Any other static host works too, such as Netlify or Cloudflare Pages.

## Playing

1. Open the address on the TV or laptop and click **Host on this screen**.
2. Guests scan the QR code, or open the address and type the 4-letter room code, then enter their name.
3. Edit the award list if you want, then click **Start the awards**.
4. For each award, everyone taps a name on their phone. Click **Reveal the winner** (or press the → key), then **Next award**.
5. At the end you get a recap of every winner, plus a **Copy the results** button.

Anyone without a phone can be added by name on the host screen. **Vote on this screen** opens a pass-around secret ballot.

## Good to know

- **Keep the host screen open.** It holds the game. If it reloads, it picks up where it left off and phones reconnect by themselves within a few seconds.
- **Have everyone join the Wi-Fi.** Phone-to-screen connections are most reliable on the same network. Some phones on cellular data can't connect directly, and this setup doesn't include a relay server for that case.
- Phones that lock or switch apps reconnect when they come back.
- Votes stay secret. The host screen shows who has voted, but not who they voted for.
