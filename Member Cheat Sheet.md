---
tags:
  - cs-club
  - handout
---

# 🔗 Link-Me Cheat Sheet

## ✨ The Golden Loop
**Edit → Save → Refresh**

| | Windows | Mac |
| --- | --- | --- |
| Save | `Ctrl + S` | `Cmd + S` |
| Refresh | `F5` or `Ctrl + R` | `Cmd + R` |
| Hard refresh | `Ctrl + Shift + R` | `Cmd + Shift + R` |
| Undo | `Ctrl + Z` | `Cmd + Z` |
| Emoji keyboard | `Win + .` | `Ctrl + Cmd + Space` |
| Inspect (DevTools) | Right-click → Inspect | Right-click → Inspect |

A **white dot** on a VS Code tab means the file isn't saved yet.

## 📁 Your Files
| File | What it is |
| --- | --- |
| `index.html` | The **content**: what's on the page |
| `style.css` | The **style**: how it looks |
| `profile.svg` | Placeholder picture. Swap in your own photo! |

Keep all of them **in the same folder**.

## 🧱 HTML

```html
<h1>Your Name</h1>
```
`<h1>` = opening tag · `</h1>` = closing tag · the text in between = content

| Code | What it does |
| --- | --- |
| `<h1>...</h1>` | Big heading |
| `<p>...</p>` | Paragraph of text |
| `<a href="https://...">...</a>` | Link. `href` = where it goes |
| `<a href="mailto:you@example.com">...</a>` | Email link |
| `<img src="me.jpg" alt="...">` | Image. `src` = which file, `alt` = description. No closing tag! |
| `class="link"` | A "name tag" so CSS can find it |
| `<!-- note -->` | Comment (the browser ignores it) |

## 🎨 CSS

```css
selector {
  property: value;
}
```
**Selector** = who · **Property** = what to change · **Value** = what to change it to
Don't forget the `:` and the `;`!

| Selector | Means |
| --- | --- |
| `body` | The whole page |
| `.link` | Everything with `class="link"` (dot = class) |
| `.link:hover` | A link while the mouse is over it |

| Property | Example | What it does |
| --- | --- | --- |
| `background-color` | `#1e1e2e` or `hotpink` | Background color |
| `color` | `white` | **Text** color |
| `font-family` | `Arial, sans-serif` | Font |
| `font-size` | `14px` | Text size |
| `font-weight` | `bold` | Bold text |
| `text-align` | `center` | Line up text left, center, or right |
| `text-decoration` | `none` | Remove the underline from links |
| `width` / `height` | `120px` | Size |
| `max-width` | `400px` | Never wider than this |
| `padding` | `16px` | Space **inside** the box |
| `margin` | `12px` / `0 auto` | Space **outside** the box (`0 auto` = center it) |
| `border` | `4px solid white` | Border: thickness, style, color |
| `border-radius` | `12px` / `50%` | Rounded corners (`50%` = circle) |
| `display` | `block` | Put each item on its own full row |
| `transform` | `scale(1.05)` | Grow or shrink |
| `transition` | `0.2s` | Animate changes smoothly |

## 🌈 Colors
- **Names:** `red`, `hotpink`, `navy`, `gold`, `teal`, ...
- **Hex codes:** `#` + 6 characters, like `#89b4fa`
- **Palette ideas:** [coolors.co](https://coolors.co)
- **VS Code:** click the little color square next to any color to open a color picker

## 🚀 Challenges
```css
/* Shadow on buttons: add to .link */
box-shadow: 0 4px 12px rgba(0, 0, 0, 0.4);

/* Gradient background: put in body instead of background-color */
background: linear-gradient(135deg, #1e1e2e, #45475a);
background-attachment: fixed;

/* Different fonts */
font-family: "Courier New", monospace;
font-family: Georgia, serif;
```

```html
<!-- Open a link in a new tab -->
<a class="link" href="https://github.com" target="_blank">💻 GitHub</a>

<!-- Tab icon: put inside <head> -->
<link rel="icon" href="profile.svg">
```

## 🛟 Something's Broken?
- **Nothing changes:** Did you save? Did you refresh? Did you unzip the folder first?
- **No styling at all:** Is `style.css` in the same folder as `index.html`?
- **CSS stops working partway down:** Look for a missing `}`, `:`, or `;` just above the first broken part
- **Broken image:** The file name must match **exactly** (capitals too). Is it in the same folder? iPhone `.HEIC` photos don't work, so use a JPG or PNG.
- **Link gives an error:** URLs need `https://` at the start
- **Everything turned into a link:** You're missing a `</a>`

## 🌍 Put It Online (GitHub Pages)
> ⚠️ It will be **public**. No phone numbers or home addresses!

1. On [github.com](https://github.com): **+** → **New repository**
2. Name it exactly `YOUR-USERNAME.github.io` → **Public** → **Create**
3. Click **"uploading an existing file"** → drag in your **files** (not the folder) → **Commit changes**
4. **Settings → Pages:** source = *Deploy from a branch*, branch = `main`, `/ (root)` → **Save**
5. Wait 1–2 min → visit `https://YOUR-USERNAME.github.io` 🎉

## 📚 Keep Learning
- [MDN Web Docs](https://developer.mozilla.org): the HTML and CSS reference
- [freeCodeCamp](https://www.freecodecamp.org): free beginner courses
- [Flexbox Froggy](https://flexboxfroggy.com): learn CSS layout with a game
