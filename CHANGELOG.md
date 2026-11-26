# Changelog

All notable changes to this project are documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/), and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

The site behind gerfaut-wallet.com: static pages built with Astro and Tailwind, in the Toundra palette, with the Bricolage Grotesque, Instrument Sans and JetBrains Mono fonts served from the site itself.

### Added

- A home page built around one screenshot of the desktop app: a centered title, a download button that names the visitor's system, the picture in full width, then seven short sections with real screenshots of the apps at their true size, and one more on how to build from source. On phones the header keeps Download in reach and folds the other entries behind a menu button.
- A download page that reads the latest mobile and desktop releases from the GitHub API, marks the card of the visitor's system, lists every file with what it is for, says how to get past Gatekeeper and SmartScreen on the first launch, and gives the checksum manifest and the minisign command to verify it. When a release has no file for a system, or GitHub does not answer, the card links to the release page instead.
- An iPhone card on the download page, next to the Android one: the app is coming soon, through TestFlight, for iOS 15 or newer, and the docs say how it will differ from Android. An iPhone visitor lands on that card, never on a file, and the home page names the iPhone as coming soon. The descriptions that search engines and link previews read name the iPhone next to Android and desktop.
- A privacy policy at /privacy, linked from the footer of every page: what the apps keep on the device, each request that leaves it and who receives it, what Tor covers, and what this site and its documentation send. The apps link to it from Settings › About.
- /releases/desktop.json and /releases/android.json, which name the latest version of each app. From version 0.1.1, the apps read them to tell you a new version is out, and the privacy policy says so.
- Security headers on every page, with a Content Security Policy that allows no inline script or style.
- A sitemap and a 404 page.
- Wrangler 4.164.0. Its local runtime now brings undici 7.30.1 itself, so the site no longer has to force that version.
