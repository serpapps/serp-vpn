# SERP VPN

> Switch IPs instantly for private, stable browsing.

SERP VPN Extension gives researchers, marketers, and privacy-conscious users a fast way to browse with different IPs without switching devices or fighting clunky VPN apps. Instead of juggling full desktop clients, it runs directly in your browser with predictable routing and clear connection status.

Choose from multiple IP locations, switch routes in a click, and keep a live view of your connection state so you always know when traffic is protected. Use it to verify search results in different regions, keep testing accounts separate, or simply keep your personal browsing isolated from work.  

👉 Get the [SERP VPN Extension here](https://serp.ly/serp-vpn)

## Features

- Multi-IP routing with curated locations for research and QA
- One-click IP switching without restarting your browser
- Clear connected/disconnected indicators on every tab
- Connection health checks to reduce surprise disconnects
- Automatic reconnection when networks flap or change
- Optional per-site rules to keep specific domains always protected
- No-logs extension layer — designed for privacy-first workflows
- Works alongside existing desktop VPNs without conflict
- Optimised routes for search, scraping, and QA workflows
- Zero analytics beacons or invasive trackers inside the extension

## Supported Browsers

SERP VPN Extension is built for modern Chromium-based browsers including:

- Chrome
- Edge
- Brave
- Opera
- Firefox

### Benefits

- Switch IPs quickly without juggling full desktop VPN clients
- Keep testing, research, and personal browsing cleanly separated
- Rely on clear connection indicators before running sensitive workflows



## FAQs

### What browsers does SERP VPN Extension support?

SERP VPN Extension is built for modern Chromium-based browsers including Chrome, Edge, Brave, and Opera. A Firefox build is planned once the initial release stabilises.

### Can I choose which IP location to use?

Yes. You can pick from available IP locations directly from the extension popup, then switch between them in a single click without restarting your browser.

### Will this slow down my browsing?

All VPN connections introduce some latency, but SERP VPN Extension prioritises stable, low-variance routes so search, QA, and normal browsing stay fast enough for daily use.

### How do I know if I am protected?

The extension shows a clear connected or disconnected indicator, plus live IP details, so you can confirm at a glance whether traffic is flowing through the VPN.

### Does the extension log my browsing activity?

No. SERP VPN Extension is designed for privacy-first workflows and does not add analytics beacons or log your browsing history inside the extension.

## Permission Justifications

| Permission | Justification |
|------------|---------------|
| `storage` | Used to store your Webshare API key, the list of available proxy servers, and the current connection status locally in the browser (chrome.storage.local). This lets SERP VPN remember your settings between sessions. No browsing content is stored or sent to us. |
| `proxy` | Used to configure the browser's proxy settings (chrome.proxy.settings) so that your traffic is routed through the Webshare proxy you select. SERP VPN only switches the proxy on or off based on your choice and does not inspect the contents of the pages you visit. |
| `tabs` | Intended for future use to react to tab changes (for example, to refresh or update tabs when the VPN connection changes). It is not currently used to read page content. You can remove this permission from wxt.config.ts before uploading if you want to minimise the requested scope. |
| `webRequest` | Used to listen for network authentication challenges via chrome.webRequest.onAuthRequired. SERP VPN uses this only to detect when a site requests proxy authentication and to attach your configured Webshare username and password. It does not inspect or modify the body of web pages. |
| `webRequestAuthProvider` | Used together with webRequest to provide proxy credentials asynchronously when the browser encounters an authentication challenge. This is required to supply your proxy username/password to the Webshare proxy server so connections succeed, and it is not used for any other purpose. |
| `<all_urls>` | Required so the extension can handle proxy authentication challenges for any website you visit. SERP VPN listens for authentication requests at the network level in order to provide your proxy credentials; it does not read, log, or modify the content of the pages you visit. |



## Related

- https://github.com/serpapps/serp-vpn
- https://gist.github.com/devinschumacher/84361cb22134d49fd875eacc2eaa9f37
