# WiFiOS — Network Dashboard

A premium, responsive WiFi/network command center designed to monitor a home network from one place.

## Current version

The first version is a static dashboard with realistic mock network data. It is intentionally structured so the mock data layer can later be replaced by a real router/network connector.

### Included

- Network overview and health score
- Live traffic visualization
- Connected device inventory
- Bandwidth usage analytics
- New-device and network alerts
- Security posture checks
- WiFi radio/channel information
- Activity history
- Router control interface placeholders
- Network Assistant with basic local-data responses
- Responsive mobile layout

## Architecture

The current build is deliberately dependency-free:

- `index.html` — application shell
- `styles.css` — responsive visual system
- `app.js` — navigation, mock network data, charts and interactions

## Next phase: real network connection

The UI does not pretend that GitHub Pages can directly control a router. Real monitoring/control should be provided by a local or server-side connector using an appropriate router API, SNMP, or a small agent running inside the LAN.

Recommended architecture:

`Router → Local Network Agent → Secure API/WebSocket → WiFiOS Dashboard`

The dashboard can then consume live devices, traffic, latency, WiFi configuration and supported router controls without exposing router credentials in browser code.

## License

Project created for the WiFiOS dashboard experiment.