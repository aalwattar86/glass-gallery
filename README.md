# Glass Gallery

A minimalist glassmorphism art gallery built as a single HTML file. It presents abstract painting-style Unsplash images in multiple visual modes, including a 3D orbit carousel, wall layout, grid layout, and focus view.

## Features

- Glassy minimalist interface with responsive layout
- 3D orbit gallery with drag rotation
- Wall, grid, and focus viewing modes
- Modal artwork detail view
- Built-in image control panel
- Unsplash link replacement workflow
- Editable title, collection, and description fields
- Browser persistence with `localStorage`
- No build step or framework required

## Project Files

- `index.html` - main publish-ready file for GitHub Pages
- `minimalist_3_d_gallery_enhanced.html` - named project copy of the same gallery
- `README.md` - project documentation

## How To Open

Open `index.html` directly in a browser.

No server is required because the project is self-contained HTML, CSS, and JavaScript.

## Gallery Controls

Use the top-right controls to switch views:

- Orbit: 3D rotating carousel
- Wall: staggered gallery wall
- Grid: clean image grid
- Focus: centered featured artwork with side previews
- Motion: toggles auto-rotation
- Edit: opens the image control panel

Keyboard shortcuts:

- `1`: Orbit view
- `2`: Wall view
- `3`: Grid view
- `4`: Focus view
- `ArrowLeft` / `ArrowRight`: move between artworks
- `Escape`: close modal or control panel

## Replacing Images

1. Click the pencil/Edit icon.
2. Choose the artwork slot.
3. Paste an Unsplash image or photo-page link.
4. Review the generated title, collection, and description.
5. Edit the text if needed.
6. Click `Apply`.

Changes are saved in the browser using `localStorage`, so they remain after refresh on the same browser and device.

Use `Reset Slot` to restore one artwork or `Reset All` to restore the full default collection.

## Unsplash Link Notes

Best supported:

- Direct image URLs beginning with `https://images.unsplash.com/...`
- Unsplash photo pages such as `https://unsplash.com/photos/red-and-blue-wallpaper-6lQDFGOB1iw`

For Unsplash photo pages, the gallery extracts the photo id and uses the photo download redirect for preview and display.

Search pages such as `https://unsplash.com/s/photos/abstract` can help generate editable text suggestions, but they are not a single image URL. For a reliable replacement, open one photo from the search results and paste that photo page link.

## Metadata Limitations

This project does not use an Unsplash API key. Without the official Unsplash API, the app cannot reliably fetch the real photographer name, official alt text, tags, or full photo metadata from every pasted link.

The control panel uses lightweight URL parsing to suggest editable text. For production-level Unsplash metadata, add an Unsplash API integration and use URLs returned by the API.

## GitHub Publishing

Suggested repository name:

```text
glass-gallery
```

Suggested GitHub Pages settings after pushing:

- Source: Deploy from a branch
- Branch: `main`
- Folder: `/root`

Because `index.html` is at the project root, GitHub Pages can serve it directly.

## Push To GitHub

From this folder:

```powershell
git init
git add .
git commit -m "Initial glass gallery"
git branch -M main
git remote add origin https://github.com/aalwattar86/glass-gallery.git
git push -u origin main
```

Create the `glass-gallery` repository under the `aalwattar86` GitHub account before running the remote/push commands.

## License

Add a license before publishing if this project will be public. The gallery code can use your chosen license, but Unsplash photos remain governed by the Unsplash License.
