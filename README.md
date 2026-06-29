# Book Store Page

A clean, responsive book store landing page built with HTML, CSS, and Bootstrap 4. Users can browse a curated list of books, view detailed descriptions, and navigate between a home listing and individual book detail pages — all without a page reload.

---

## Live Demo

> Open `index.html` in any modern browser — no build step or server required.

---

## Features

- **Home Page** — showcases a featured "Popular Book" alongside a "Recommended Books" section
- **Book Detail Pages** — each book has a dedicated detail view with a cover image, description, author, and a *Buy Now* CTA
- **Single-Page Navigation** — sections are shown/hidden dynamically via JavaScript; no routing library needed
- **Responsive Layout** — built on Bootstrap 4's flexbox grid, adapts gracefully to different screen sizes
- **Back Navigation** — every detail page includes a *Back* button that returns the user to the home listing

---

## Books Included

| Title | Author |
|---|---|
| Wings of Fire *(Popular Pick)* | Arun Tiwari (autobiography of Dr. APJ Abdul Kalam) |
| The 3 Mistakes of My Life | Chetan Bhagat |
| Harry Potter and the Sorcerer's Stone | J.K. Rowling |

---

## Project Structure

```
book-store-page/
├── index.html      # Main HTML file — all sections and navigation logic
└── styles.css      # Custom styles layered on top of Bootstrap
```

---

## Getting Started

### Prerequisites

No installation needed. A modern web browser (Chrome, Firefox, Edge, Safari) is all that's required.

### Run Locally

```bash
# Clone the repository
git clone https://github.com/Anandu-12233/book-store-page.git

# Navigate into the project folder
cd book-store-page

# Open the page
open index.html        # macOS
start index.html       # Windows
xdg-open index.html    # Linux
```

Or simply drag `index.html` into your browser.

---

## Built With

| Technology | Purpose |
|---|---|
| HTML5 | Page structure and content |
| CSS3 | Custom styling (`styles.css`) |
| [Bootstrap 4.5.2](https://getbootstrap.com/docs/4.5/) | Responsive layout, buttons, and utility classes |
| jQuery 3.5.1 | DOM manipulation (via Bootstrap dependency) |
| Popper.js 1.16.1 | Tooltip/popover positioning (via Bootstrap dependency) |
| CCBP UI Kit | Supplementary UI utilities |

---

## How the Navigation Works

All book sections (`#sectionBookStoreHome`, `#sectionWingsOfFireBookDetails`, etc.) are rendered in the DOM at load time. The `display()` helper from the CCBP UI Kit shows the target section and hides the rest when a *Read Now* or *Back* button is clicked:

```html
<button onclick="display('sectionWingsOfFireBookDetails')">Read Now</button>
```

This gives the feel of page transitions without any JavaScript routing framework.

---

## Customisation

- **Add a new book** — duplicate an existing `recommended-book-container` block in `index.html`, update the image URL, title, and author, and create a matching detail section.
- **Change colours or fonts** — edit `styles.css`; Bootstrap utility classes can be overridden there.
- **Swap book images** — replace the `src` attributes on `<img>` tags with your own hosted image URLs.

---

## License

This project is open source and available under the [MIT License](LICENSE).

---

## Acknowledgements

- Book cover images hosted via [CCBP](https://ccbp.in/) static assets
- UI inspiration from classic e-commerce book listing pages
