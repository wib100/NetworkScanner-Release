# Changelog

## 0.5b

- Split the generic "Smart Home" category into Energy, Heating, Hub, Gate and Outlet
- Device aliases and notes survive a changed IP address (stable device identity)
- Optional automatic refresh while the app is open (1, 2, 5, 10 or 15 minutes, default off)
- Faster scans: devices that already identified themselves skip the full port scan and HTTP probing
- NetBIOS names are collected with one broadcast query instead of one query per device
- Removed an unused SMB probe that never produced results

## 0.3h

- Test release for final validation of the in-app update flow from 0.3g
- No feature changes beyond the already shipped 0.3g update-flow fixes

## 0.3g

- Refined device list badges and indicators to avoid overlap in dense rows
- Replaced the alias text chip with a compact tag icon in the device list
- Expanded demo mode so NEW, GONE, alias, and note states are visible in screenshots and presentations
- Enabled deep scan behavior by default and removed the extra setting toggle
- Hardened the in-app update flow on modern Android, including permission resume for notifications and APK installation

## 0.3f

- Added option to show discovered devices live during an active scan
- Improved scan list stability by preventing layout jumps during live updates
- Added a visible alias badge when a custom device name is shown
- Improved list update performance by refreshing only affected device rows

## 0.3e

- Improved device classification consistency and offline analysis traceability
- Refined the radar scan animation for a more realistic sweep and target glow
- Added device counts to grouped device sections
- Added scan history housekeeping and kept only recent scans per network
- Improved scan screen behavior when starting a new scan
