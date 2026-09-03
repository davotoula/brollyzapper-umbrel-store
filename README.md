# BrollyZapper — Umbrel community app store

A preview channel for [BrollyZapper](https://github.com/davotoula/brollyzapper) while the
[official App Store submission](https://github.com/getumbrel/umbrel-apps/pull/6049) is under review.

BrollyZapper adds Nostr zap receiving (NIP-57) and Nostr Wallet Connect (NIP-47) to the
Lightning node you already run on umbrelOS. It is receive-only until you turn sending on.

## Before you install

- umbrelOS 1.x with the **Lightning Node** app installed and synced. BrollyZapper reads that
  node's certificate and admin macaroon through Umbrel's own app exports; it does not run a
  node of its own.
- A domain that reaches your box over HTTPS, for the Lightning address. Setting that up is
  covered in the operator guide inside the app.

## Install

1. In the umbrelOS **App Store**, click the three dots (top right) → **Community App Stores**.
2. Paste `https://github.com/davotoula/brollyzapper-umbrel-store` and click **Add**.
3. Open the new store and install **BrollyZapper**.
4. Open the app from your dashboard. Set your domain, address name and relays on the Settings page.

A fresh install is receive-only: the credential it holds cannot move a satoshi. Sending is off
until you complete the authorisation step the app walks you through, which bakes a second,
separately revocable credential with a spending ceiling you choose. That is by design, not a fault.

## Updates

New versions are pushed to this repository. Your box picks them up within a few minutes and
shows an update on the app's tile, exactly as for any other app.

Versions ending in `-rc1`, `-rc2`… are pre-releases: a pull request published for testing before
it merges. They are built by the same workflow from the same repository, pinned by digest, and
replaced by the numbered release once it ships.

## When the official listing lands

The app id here is the same as the one submitted to the official App Store, so your data and
settings are the same app. We will document the switch-over here once it has been tested.

## Support

Issues and questions: https://github.com/davotoula/brollyzapper/issues — please redact
macaroons, keys, connection URIs and preimages from anything you paste.
