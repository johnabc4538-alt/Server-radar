# Server Radar

A responsive, browser-based dashboard for tracking public FiveM and Minecraft server status.

## Run it

Open `index.html` in a modern browser, or publish the repository with GitHub Pages. No build step, framework, or API key is required. The dashboard uses browser `fetch()` requests to public status APIs, so it works best when hosted on a web server (for example, GitHub Pages) rather than opened as a local file.

## Features

- Choose between GTA Online, FiveM, and Minecraft.
- Add FiveM or Minecraft servers by hostname/IP and optional port.
- View online/offline state, player counts, and available server details.
- Automatically refresh tracked servers every five minutes; use **Check now** for an immediate refresh.
- Keep your tracked server list in browser local storage.
- Responsive layout with game artwork hosted by Unsplash.

## Status sources and limitations

- Minecraft status: [mcsrvstat.us API](https://api.mcsrvstat.us/).
- FiveM status: public FiveM server listing endpoint at `servers-frontend.fivem.net`.
- Status APIs are third-party services. Availability, rate limits, CORS behavior, and returned fields can change. If an API blocks browser requests, host a small server-side proxy and update the fetch endpoint.
- GTA Online does not expose a public per-server IP/player-count API, so the site explains this rather than showing made-up live data.
- Server images are loaded from Unsplash; an internet connection is needed for them and for live status checks.

## GitHub Pages

In the repository, open **Settings → Pages**, choose **Deploy from a branch**, select `main` and `/ (root)`, then save. GitHub Pages will publish `index.html`.
