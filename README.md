# PokiSubmission

Private portal for Poki submissions, published with GitHub Pages. It is its own git repo,
ignored by the BrowserGames repo that contains this folder.

- `index.html`: the test harness. It embeds a game in an iframe inside a scrolling page, the
  way Poki does, and has manual checks for canvas sizes (A5), scrolling (A6), blocked
  storage (A7) and network requests (A8).
- `<Game>/`: a web build of one game, for example `PuzzleProto/`. Add each game to `GAMES`
  in `index.html`.
- `.nojekyll`: tells GitHub Pages to serve the files as they are.

The harness and the game must be on the same origin, so keep every game build in this repo.

## Publish

The `main` branch is the only branch, and GitHub Pages serves it from the root
(Settings > Pages > Deploy from a branch > `main`, `/ (root)`).

To update a game, replace its folder with the new web build, then commit and push.
