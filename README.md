# Vaibhav Bhagat — Portfolio
 
Personal portfolio website of Vaibhav Bhagat, a 3rd-year Computer Science Engineering student at BIT Ballarpur.
 
The site is a single `index.html` file with inline CSS and a small amount of JavaScript. There is no build step, no framework and no dependencies beyond one Google Fonts stylesheet.
 
The visual style is a calm, matte, folded-paper look: flat pastel color fields, deep-ink type and plenty of empty space.
 
## Sections
 
| Section | What it contains |
|---|---|
| Home | Two-line name title, a numbered section list on the left and a "See my work" button |
| About | Short introduction |
| Skills | C, C++, Java, HTML & CSS, Python, SQL |
| Projects | Placeholder until the first project is added |
| Contact | Placeholder text and a link to GitHub |
 
## Features
 
- Background color crossfades between pastel colors as you scroll to each section
- Fixed vertical section list with a progress bar that follows the active section
- Round menu button that opens a full-screen ivory overlay (close it with the button or the Escape key)
- Responsive layout for desktop, phones in portrait and short landscape screens
- Keyboard focus outlines on all links and buttons
- Respects the reduced-motion setting (transitions and smooth scrolling are turned off)
## Design system
 
### Font
- **Figtree** from Google Fonts
- Weight 500 for headings, labels, buttons and navigation
- Weight 400 for body text
- Fallback: `system-ui, sans-serif`
### Colors
 
| Token | Value | Used for |
|---|---|---|
| `--ink` | `#1D1B2E` | All text and buttons |
| `--ivory` | `#FAF6F0` | Button text and the menu background |
| `--content` | `#FBFAF8` | Long content sections |
| `--grey` | `#55535f` | Paragraphs |
| `--grey-sm` | `#77757f` | Small descriptions |
 
### Pastel page colors
 
| Section | Page color | Card color |
|---|---|---|
| Home | `#F7C6B2` | `#FBDDD0` |
| About | `#BEE5D3` | `#D7F0E4` |
| Skills | `#B7D3F3` | `#D2E3F8` |
| Projects | `#F6E3A1` | `#FAEDC4` |
| Contact | `#CDBBF2` | `#DFD3F7` |
 
Each section stores its colors in `data-bg` and `data-card` attributes. The script reads them and updates the page background and card color as you scroll.
 
### Sizing
- `--u` is the design unit: `100vw / 1440` on desktop and `100vw / 390` on phones.
- Almost every size is written as a multiple of `--u`, so the layout scales with the screen width.
- The hero title size is `min(9.9vw, 19vh)` on desktop and `13.125vw` on phones.
### Fixed layout positions (desktop)
- Logo: 42u from the left, 36u from the top
- Menu button: 42u from the right, 36u from the top, 58u wide
- Footer links: 46u from the left, 36u from the bottom
- Section list: 46u from the left, vertically centered
- Hero title: centered at 56% of the viewport width
- Hero button: left `56vw − 96u`, top `71vh − 33u`
## Project structure
 
```
.
├── index.html   # the whole site: markup, styles and script
└── README.md
```
 
## Customizing
 
1. **Text and sections:** edit the `<section>` blocks inside `<main>`. Each one needs an `id` plus `data-bg` and `data-card` attributes. If you add a section, also add a link in the `#tabs` list and the `#menu` overlay.
2. **Skills:** add or remove `<li>` items inside `.skills`.
3. **First project:** replace the placeholder inside the `#projects` panel with your own title, description and link.
4. **Contact:** replace the GitHub button in `#contact` with a `mailto:` link when you want to show an email address.
5. **Colors:** change the hex values in `:root` (and in the `data-bg` and `data-card` attributes for the pastel colors).
## Run locally
 
Open `index.html` in any modern browser. An internet connection is needed only to load the Figtree font. Without it, the site falls back to the system font.
 
## Deploy with GitHub Pages
 
1. Make sure the file is named `index.html` and sits in the root of the repository.
2. Go to **Settings → Pages**, choose the `main` branch and the root folder, then save.
3. For the site to appear at `https://<username>.github.io`, the repository must be named exactly `<username>.github.io`. Any other name publishes it at `https://<username>.github.io/<repository-name>/`.
## Browser support
 
Current versions of Chrome, Edge, Firefox and Safari.
 
## Author
 
**Vaibhav Bhagat** — [GitHub](https://github.com/Vaibhav-0307)
 
