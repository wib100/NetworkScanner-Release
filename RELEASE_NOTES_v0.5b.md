# Network Scanner 0.5b

## Highlights

- **Finer device categories.** The single "Smart Home" bucket is gone. Devices that identify themselves
  now land in **Energy** (solar inverters, smart meters), **Heating** (heat pumps), **Hub** (Zigbee
  coordinators, home automation servers), **Gate** (garage and door controllers) and **Outlet**
  (wall plugs). On a 60-device home network the generic bucket dropped from 17 devices to 3.

- **Aliases and notes survive a changed IP address.** Devices are now tracked by the identity they
  announce (service UUID, hostname, NetBIOS name) instead of their IP. When the router hands out a new
  address, your custom name and notes stay attached.

- **Automatic refresh.** While the app is open it can rescan every 1, 2, 5, 10 or 15 minutes
  (default: off). New and disappeared devices show up without pulling to refresh.

- **Faster scans.** Devices that already identified themselves are no longer probed with the full
  port scan and HTTP probing. On a 60-device network a scan dropped from about 47 s to 36 s, and the
  HTTP probing phase from 12 s to 7 s.

- **Quieter, shorter name lookup.** NetBIOS names are collected with a single broadcast query instead
  of one query per device; only devices that stayed silent get an individual query.

## Compatibility

- Android 8.0 and newer (minSdk 26).
- Signed with the same key as 0.3h, so it installs as an update over the previous version and keeps
  your saved names, notes and scan history.

## Notes

- Some devices answer identification requests only occasionally. A device can be named in one scan and
  appear unnamed in the next – that is device behaviour, not a classification bug.
- Android does not expose hardware addresses of other devices to apps (Android 10 and newer), so
  vendor detection relies on what a device announces about itself.
