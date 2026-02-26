## v0.1 – Initial public build
- Single-page Indie Maps setup with retro chrome UI, MapLibre map, OpenFreeMap Liberty tiles, and inline styling for static hosting.
- Two-step search flow: primary location finder plus optional destination input that toggles with `+`/`×`, shared results list with start/destination badges, recent-search history, and query parameters for sharing (`?s=`/`&d=`).
- OSRM routing once both locations exist, with distance/time summary, unit toggle, clear button, and cached routes preserved while the destination field is hidden.
- Persistent user experience: localStorage for history, queries, route summary; geolocation-based blue dot that follows the user; URL syncing; ability to restore route from params.
- iOS/web-app friendly metadata plus favicon/Apple touch icon for homescreen shortcuts.
