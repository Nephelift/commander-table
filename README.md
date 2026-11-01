# Commander Table

A standalone Windows tabletop for manual Magic: The Gathering Commander games with up to four players.

## Download

[Download Commander Table for Windows x64](https://github.com/Nephelift/commander-table/releases/latest/download/Commander-Table-Windows-x64.zip)

1. Download the ZIP from Releases.
2. Extract the entire ZIP into a writable folder.
3. Open **Commander Table.exe**. No separate Node.js installation or EDHPlay account is needed.

Windows x64 only. This personal app is unsigned. Keep the entire extracted folder together.

## Play

Import a text deck list in **My decks**. Card lookup and uncached artwork require internet access and use Scryfall. Deck legality and game rules are enforced by the players.

Choose **Playtest** to practice or **Host a table** to play with friends. Friends open their own copy, choose **Join a room**, and enter the host address and room code. The host starts the game after everyone chooses a deck.

On the same LAN, use the address shown in the lobby. Across networks, use a reachable private VPN address or configure TCP port 47652 forwarding. A room code alone cannot cross a router. The built-in game connection is HTTP/WebSocket; use a trusted LAN or private VPN. Keep the host app open.

Each player sees their own hand; other hands show card backs unless explicitly revealed. The hosting computer stores the complete game state, so play with a trusted host. Solo seat-switching follows the same visual perspective.

## Controls and customization

- Drag cards around the battlefield and between zones, including from a card-view window.
- Click a permanent to tap or untap; double-click a hand or commander card to play it.
- Right-click cards for actions, counters, reveals and zone changes.
- Counter markers: left-click adds one, right-click removes one.
- Press N for tokens; left-click creates, right-click removes a matching token.
- D draws, S shuffles, U untaps all, V views the library, Space passes the turn.
- The game menu contains the full shortcut reference.
- **Settings** offers custom local playmats/sleeves and dark, light and midnight skins. Appearance is local to each device.
- Recent tables can be removed from the list and the last removal undone.

## Save data and updates

Decks, saved games, appearance images and reconnect information live in **UserData**, beside the executable. Back up this entire folder. When updating, close the app and replace application files while preserving UserData. Release downloads contain no player save data.

## Source and validation

The release includes a separate application source ZIP. It contains the Electron desktop shell, Socket.IO host, interface and tests. With Node.js installed: `npm ci`, `npm run build`, `npm test`, `npm run package`. The Windows package is produced in `dist/win-unpacked`.

Version 0.3.2 passed 12 automated tests, including four connected clients, private-hand filtering, authorization, reveal/hide, reconnect, saved-state restore and stale inspection state. Native desktop checks covered deck editing, card movement, counters, tokens, custom images and viewer dragging. Connections between separate households have not been tested.

This is an independent, unofficial fan tabletop. It does not enforce Magic rules automatically and is not affiliated with Wizards of the Coast, Scryfall or EDHPlay. Magic and card artwork belong to their respective owners. Third-party runtime license notices are included in the Windows package.
