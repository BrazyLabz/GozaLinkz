# GozaLinkz prototype

A mobile-friendly creator link hub with an embedded YouTube preview, social buttons, and free app cards.

## Update the page

Open `index.html` and edit the `CONFIG` object near the bottom:

- `youtubeChannelId` must be set to the channel's stable YouTube ID for automatic refresh. Find it in YouTube Studio under Settings → Channel → Advanced settings. With a valid ID, GozaLinkz checks the latest public upload on page load using the public YouTube RSS feed through rss2json. Automatic refresh depends on that free service.
- `video.url` is the fallback video used when automatic lookup is off or unavailable. `video.title` controls the player title.
- The **See latest videos** link always opens the channel's Videos tab, where YouTube itself lists current uploads.
- Add up to six icon buttons in `socials` and up to five text buttons in `links`.
- Add public destinations to the app cards in `apps`. The three app cards use their icons from this folder.

When opened directly as a local `file://` page, the video thumbnail opens YouTube in a new tab because embedded YouTube playback may fail without a normal website origin. On a hosted HTTPS page, the thumbnail uses the embedded player; **Open video on YouTube** remains available as a fallback.

The page has a simple spinning-logo intro, smooth reveal animations, and a rounded header that stays hidden over the hero and appears after scrolling past it. Receipt, playlist, and other visitor data is not collected by this link hub.

## Publish it so anyone can access it

Upload the contents of this folder to a static web host that provides HTTPS, such as GitHub Pages. Include `index.html`, `manifest.webmanifest`, `sw.js`, `goza-logo.png`, `apple-touch-icon.png`, `app-icon-192.png`, `app-icon-512.png`, `coffee-icon.png`, `merch-icon.png`, `braindumpz-icon.png`, `tuneloopz-icon.png`, and `recibin-icon.png`. Enable Pages in the repository settings and use the resulting HTTPS URL as your public GozaLinkz link.


