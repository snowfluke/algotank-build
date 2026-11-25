# AlgoTank offline build

This repository holds the built files of the AlgoTank tank workshop, version 1.0.0. It holds no source code.

In the workshop, a player builds a play style for a toy water tank from rules, then runs test matches against bots. The game runs in the browser and needs no server, so it also works on a game portal that blocks outside requests. The play styles and the tank's look are saved in the browser's localStorage. When the browser blocks storage, they stay until the page closes.

The online parts of AlgoTank (arenas, accounts and the monthly league) need the game server, so this build leaves them out.

## Run it

Serve the folder with any static web server and open `index.html`. All links are relative, so the folder can sit at any path. Opening `index.html` straight from the disk (`file://`) does not work, because browsers do not load module scripts from `file://`.

```bash
npx serve .
```

## Game portal ZIP

The release `v1.0.0` has the file `algotank-1.0.0.zip` attached. It holds the files of this folder except `README.md` and `package.json`, with `index.html` at its root.

A portal that shows the game in an `<iframe sandbox="allow-scripts">` without `allow-same-origin` must send `Access-Control-Allow-Origin` with each file, because the page then has the origin `null` and a module script needs CORS. This is true of every game built with Vite or other ES modules.

## Licenses

- The game: MIT, see `LICENSE`.
- The fonts Figtree and Fredoka: SIL Open Font License 1.1, see `licenses/`.
- The country flags in `flags/`, from flag-icons: MIT, see `flags/LICENSE.txt`.
