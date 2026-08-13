# SpotifyBridge

SpotifyBridge brings live Spotify playback data and lyrics into TouchDesigner.

## Download

SpotifyBridge is free to download:

[**Download SpotifyBridge v2.5.0 (.tox)**](https://raw.githubusercontent.com/merterbil/SpotifyBridge/main/releases/SpotifyBridgeV2.5.0.tox)

Versioned builds are stored in the repository's [`releases` folder](https://github.com/merterbil/SpotifyBridge/tree/main/releases). No Patreon membership or payment is required.

## How to Use

1. Download `SpotifyBridgeV2.5.0.tox`.
2. Open a fresh TouchDesigner project and drag the `.tox` into the network.
3. Open the component's **Spotify Setup** parameter page.
4. Enter your own Spotify **Client ID** and **Client Secret**.
5. Press **Authenticate with Spotify** and complete authorization in your browser.
6. Start Spotify playback. SpotifyBridge will expose the current playback data, lyrics, and prepared public output operators inside the component.

## Authentication Cache

After successful authorization, SpotifyBridge stores its Spotify authentication cache in the TouchDesigner project's VFS so the session can refresh without requiring a new login each time.

Press **Disconnect / Clear Cache** on the **Spotify Setup** page whenever you want to disconnect and delete that stored VFS cache. Use this before sharing or exporting a project that has been authenticated.

## GitHub-Based Updates

SpotifyBridge checks its official GitHub manifest once when the component is loaded. You can disable **Auto Check on Load** or run **Check for Updates** manually from the **Updates** parameter page.

When an update is available, press **Download Update** to download the current release. The updater does not silently replace components or modify user projects.

The main idea behind this release is reusable: other TouchDesigner developers can adapt the same GitHub manifest and version-check pattern for their own `.tox` tools. Each developer can publish a manifest and versioned `.tox` files in their own GitHub repository, then point their component's checker to that repository. This gives independently distributed tools a simple update channel without requiring a separate manager component.

The manifest can describe the tool ID, latest version, public download URL, release page, publisher, and TouchDesigner compatibility. SpotifyBridge's [public manifest](https://github.com/merterbil/SpotifyBridge/blob/main/manifest.json) is available as a working reference.

## Compatibility

The current release was built and tested with TouchDesigner 2025.33070 on macOS.

A TouchDesigner 2025-exported `.tox` should not be treated as TouchDesigner 2023 compatible. A separate TD 2023 export and independent Windows/macOS testing are required before claiming broader compatibility.

## Security

Release builds must never contain Spotify access tokens, refresh tokens, client secrets, populated cache files, or user information. Users enter their own Spotify credentials locally.

## Support

Use [GitHub Issues](https://github.com/merterbil/SpotifyBridge/issues) for reproducible bugs and documentation problems. Do not post Spotify credentials, tokens, or cache files.

You can also follow and support my TouchDesigner work on [Patreon — merderbil](https://www.patreon.com/merderbil).

The downloadable `.tox` is free to download and use. No open-source license has been declared for its internal code unless explicitly stated.
