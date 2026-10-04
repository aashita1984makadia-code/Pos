Nexrise POS Responsive Upgrade

Files:
1. index.html — responsive PC/main billing page. The camera scanner has been removed.
2. scanner.html — separate responsive mobile barcode/QR scanner.
3. README.txt — setup and multi-device networking notes.

Login:
Username: admin
Password: 1234

Important multi-device note:
A browser's BroadcastChannel/localStorage cannot reliably deliver data between two separate physical devices. The included scanner therefore has the UI and scanning logic, but true phone -> PC delivery requires both pages to be served by the same POS web server plus a WebSocket/Socket.IO relay.

Recommended production flow:
Mobile scanner -> WebSocket server -> PC billing page -> product lookup -> cart -> billing.

The existing local-storage inventory and saved-bill data remain browser-local.
