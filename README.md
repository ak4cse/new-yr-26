# New Year 2026 Web Experience

A polished, interactive New Year greeting page built with HTML, CSS, and vanilla JavaScript. The experience combines animated visuals, personalized messages, background music, sound effects, confetti, and small easter eggs into a single static web page that is easy to host and share.

## Features

- Personalized greeting through a URL query parameter.
- Animated starfield, shooting stars, cursor trails, and floating effects.
- Tap/click-driven message sequence for a cinematic greeting flow.
- Background music toggle with a separate confetti sound effect.
- Lucky planet interaction with surprise messages.
- Double-tap heart burst animation.
- Secret `2026` keyboard code for party mode.
- Fully static implementation with no build step required.

## Project Structure

```text
.
|-- index.html       # Main web page with HTML, CSS, and JavaScript
|-- audio.mp3        # Background music track
|-- confettti.mp3    # Confetti sound effect used by the page
`-- README.md        # Project documentation
```

## Getting Started

You can open the project directly in a browser:

```text
index.html
```

For a more realistic local preview, serve the folder with any static file server:

```bash
python -m http.server 8000 --bind 127.0.0.1
```

Then open:

```text
http://127.0.0.1:8000/
```

## Personalization

Add a `name` query parameter to personalize the opening greeting:

```text
http://127.0.0.1:8000/?name=Rahul
```

This changes the first message to:

```text
Hello, Rahul.
```

If no name is provided, the page falls back to:

```text
Hello, There.
```

## Usage Notes

- The page starts audio only after the first user tap or click, which matches modern browser autoplay rules.
- The confetti animation is powered by the `canvas-confetti` CDN package.
- Google Fonts are imported from the Google Fonts CDN.
- An internet connection is recommended for the CDN-hosted confetti script and fonts.
- If you need the page to work fully offline, download and serve those external dependencies locally.

## Customization

Most content can be edited directly in `index.html`:

- Update the message sequence in the `story` array.
- Change colors, spacing, and animations in the `<style>` block.
- Replace `audio.mp3` to use a different background track.
- Replace `confettti.mp3` to use a different celebration sound effect.
- Update the developer credit near the bottom of the HTML.

## Deployment

Because this is a static website, it can be deployed to any static hosting service, including:

- GitHub Pages
- Netlify
- Vercel
- Cloudflare Pages
- Any standard web server

Upload the full project folder and make sure `index.html`, `audio.mp3`, and `confettti.mp3` remain in the same directory.

## Browser Support

The page is designed for modern desktop and mobile browsers. It uses standard HTML5 audio, CSS animations, URL search parameters, and vanilla JavaScript.

## License

No license file is currently included. Add a license before distributing or accepting public contributions.
