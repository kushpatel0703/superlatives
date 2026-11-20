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

## Chaos features (toggle them on the setup screen)

- **🎰 Snitch Roulette:** strikes at random. A wheel picks one voter and shows their vote on the TV.
- **⚖️ Defend Yourself:** some winners get 30 seconds to plead their case. The table votes on their phones: guilty +2, acquitted −1.
- **⚡ Double Down:** each player gets one ×2 vote per 7 awards.
- **🔮 Oracle Bets:** after voting, guess the winner. +1 if you're right.
- **✍️ Write-ins:** halfway through, everyone writes one award. They're added to the end, and the author is revealed.

Scoring: 1 point per vote you get, +2 per award won, plus the Oracle and courtroom points above. Nobody can vote for themselves.

At the end the game hands out awards worked out from how people voted: The Grudge, The Stalker, The Sheep, The Lone Wolf, The NPC, The Prophet, Repeat Offender, The Speedrunner and The Sloth. Every phone gets a yearbook card.

**Running the night:** press **P** or click Pause to freeze the game while people talk. Tap 👑 next to a phone player to make them co-host, which gives them Pause and Next buttons. After the game starts the room locks (🔒), so new arrivals need your OK to join.

## Good to know

- **Keep the host screen open.** It holds the game. If it reloads, it picks up where it left off and phones reconnect by themselves within a few seconds.
- **Have everyone join the Wi-Fi.** Phone-to-screen connections are most reliable on the same network. Some phones on cellular data can't connect directly, and this setup doesn't include a relay server for that case.
- Phones that lock or switch apps reconnect when they come back.
- Votes stay secret. The host screen shows who has voted, but not who they voted for.
