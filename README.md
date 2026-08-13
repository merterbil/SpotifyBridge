SpotifyBridge

SpotifyBridge brings live Spotify playback data and lyrics into TouchDesigner.

DISTRIBUTION

SpotifyBridge is a paid merterbil tool. This public repository contains documentation, issue tracking, release notes, and update metadata. The downloadable .tox remains available through the official Patreon page:

https://www.patreon.com/cw/merderbil

Paid .tox files are not published in this repository.

COMPATIBILITY

TouchDesigner 2023 and newer on Windows and macOS are the compatibility targets. Exact tested builds will be listed with each release. A distributable .tox intended for both generations should be exported from TouchDesigner 2023 and independently verified in TouchDesigner 2023 and 2025.

SECURITY

Release builds must never contain Spotify access tokens, refresh tokens, client secrets, populated cache files, or customer information. Users enter their own Spotify credentials locally.

VERSIONING

SpotifyBridge uses semantic versioning: MAJOR.MINOR.PATCH. Each public release record will list its version, minimum TouchDesigner build, tested systems, release notes, and official Patreon download page.

UPDATES

A separate Merterbil Manager component is planned to read official version metadata and notify users when updates are available. It will not silently replace .tox files.

SUPPORT

Use GitHub Issues for reproducible bugs and documentation problems. Do not post Spotify credentials, tokens, cache files, or paid .tox files.

Copyright (c) merterbil. All rights reserved. No license is granted for the paid .tox file or its internal code unless explicitly stated.

