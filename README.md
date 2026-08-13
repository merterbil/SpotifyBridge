# SpotifyBridge

SpotifyBridge brings live Spotify playback data and lyrics into TouchDesigner.

## Download

SpotifyBridge is free to download:

[**Download SpotifyBridge v2.4.7 (.tox)**](https://raw.githubusercontent.com/merterbil/SpotifyBridge/main/releases/SpotifyBridgeV2.4.7.tox)

Versioned builds are stored in the repository's [`releases` folder](https://github.com/merterbil/SpotifyBridge/tree/main/releases). No Patreon membership or payment is required.

## Updates

SpotifyBridge checks its official GitHub manifest once when the component is loaded. You can disable **Auto Check on Load** or run **Check for Updates** manually from the **Updates** parameter page.

The update checker only reports availability and opens the official download page. It does not silently replace components or modify user projects.

## Compatibility

The current release was built and tested with TouchDesigner 2025.33070 on macOS.

A TouchDesigner 2025-exported `.tox` should not be treated as TouchDesigner 2023 compatible. A separate TD 2023 export and independent Windows/macOS testing are required before claiming broader compatibility.

## Security

Release builds must never contain Spotify access tokens, refresh tokens, client secrets, populated cache files, or user information. Users enter their own Spotify credentials locally.

## Support

Use [GitHub Issues](https://github.com/merterbil/SpotifyBridge/issues) for reproducible bugs and documentation problems. Do not post Spotify credentials, tokens, or cache files.

You can also follow and support my TouchDesigner work on [Patreon — merderbil](https://www.patreon.com/merderbil).

The downloadable `.tox` is free to download and use. No open-source license has been declared for its internal code unless explicitly stated.
