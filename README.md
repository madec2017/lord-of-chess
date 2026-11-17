# Lord of Chess

A browser-based 3D chess game built around the standard starting position, a walnut-framed board, textured Staunton-inspired pieces, and algebraic board coordinates.

**Play it:** https://madec2017.github.io/lord-of-chess/

## Play locally or invite a friend

Use the board to select a piece and destination. Legal moves, castling, en passant, promotion, check, and checkmate are handled by `chess.js`. **New game** resets to the standard position; **Undo** is available for local play.

Choose **Friend room** to create a room. The host can share its 8-digit PIN, QR code, or copied invite link. The invited player joins by scanning/opening the link or entering the PIN. When the room starts, colors are assigned at random and the board rotates for each player. A room admits one invited opponent; additional connections are refused. The host can end the room and the guest can leave it.

## Current scope and limitations

Friend rooms use PeerJS for peer-to-peer data connections and PeerJS Cloud for signaling. The room PIN is an invitation code, not an account identity or a ranked-security credential. The host’s browser validates incoming moves and relays the board state, so the host must keep the page open; there is not yet a trusted game server, account system, saved profile, persistent stats, or match history. Do not treat these rooms as cheat-proof competitive/ranked games.

The single-file `index.html` loads Three.js, `chess.js`, PeerJS, and QR generation from public CDNs, so an internet connection is required. The knight mesh is embedded in the HTML; its source and MIT attribution are noted in the file.
