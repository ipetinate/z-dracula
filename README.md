# Z Dracula Theme for Zed

Theme extension for the Zed editor.

## Considerations

This theme is a modification of the official Dracula theme, my utmost respect to Zeno Rocha (my fellow Brazilian) and the Dracula developers. I've been using this theme for over 7 years and I really like it, but the official theme for Zed had dark panels that contrasted too much with the background of the code panel.
This theme applies consistency to the background colors of the panels, terminal, and other areas, making them the same color as the background of the code editor.
Visually it is less heavy and more pleasing to the eye, without tiring after long coding sessions.
This color configuration is very reminiscent of Dracula for VS Code. But it was a visual modification of mine, in order to suit my preference.
If you prefer the normal Dracula, I recommend using the official theme (which can be found here).

## Structure

- `extension.toml`: Extension manifest with metadata (id, name, version, authors, description, repository).
- `themes/z-dracula.json`: Theme color definitions used by Zed.
- `LICENSE`: Project license file (required for publishing in the official registry).
- `README.md`: Project documentation and setup instructions.

## How to use locally (Dev Extension)

1. Open Zed.
2. Go to `Extensions`.
3. Click `Install Dev Extension`.
4. Select the `z-dracula` folder.

## How to publish this theme to the Zed Extensions Store

1. Ensure your theme repository is public and includes a supported license file at the root (for example: MIT, Apache-2.0, BSD, GPL/LGPL, or zlib).
2. Update `extension.toml` with the correct metadata and bump the `version` before publishing.
3. Fork and clone `zed-industries/extensions`, then initialize submodules:

```bash
git clone https://github.com/<your-username>/extensions
cd extensions
git submodule init
git submodule update
```

4. Add your theme repository as a submodule inside `extensions/`:

```bash
git submodule add https://github.com/<your-username>/z-dracula.git extensions/z-dracula
git add extensions/z-dracula
```

5. Add an entry for your extension in the top-level `extensions.toml`:

```toml
[z-dracula-theme]
submodule = "extensions/z-dracula"
version = "0.1.0"
```

6. Run `pnpm sort-extensions` to keep `extensions.toml` and `.gitmodules` sorted.
7. Commit your changes and open a pull request to `zed-industries/extensions`.
8. After the pull request is merged, your theme is packaged and published in the Zed Extensions Store.

## Preview

<img src="https://raw.githubusercontent.com/ipetinate/z-dracula/refs/heads/main/docs/images/preview.png" alt="Alt text" style="float:right; margin: 0 0 10px 10px;">

