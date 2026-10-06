---
tags:
  - cs-club
  - workshop
  - html
  - css
length: 60 min core + 15 min optional publishing
---

# 🔗 Link-Me: Build Your Own Linktree

> [!info] At a glance
> **Audience:** Beginners with zero web dev experience
> **Length:** ~60 min core, +15 min if you publish online
> **What they leave with:** A personal link page they built themselves (and optionally a live URL they can put in their Instagram/LinkedIn bio)
> **Hand out:** the `linktree-starter` folder (zipped) + [[Member Cheat Sheet]]
> **Keep for yourself:** `linktree-finished` is your demo, and it's the catch-up copy for anyone who falls behind
> **On screen:** `Link-Me Slides.pptx` follows these notes section by section. Each step has its own slide, so leave it up while people work.

**How to read these notes:**

> [!quote] Say
> Things to say out loud. Paraphrase them, no need to read word for word.

> [!example] Do
> What to show on the projector.

> [!warning] Watch out
> The spots where beginners usually get stuck. Slow down here.

> [!check] Checkpoint
> Stop and check that the room is caught up before moving on.

---

## ⏱️ Run of show

| Time | Section | Steps |
| ---- | ------- | ----- |
| 0:00 | [[#1. Hook & Intro]] | |
| 0:05 | [[#2. Setup]] | |
| 0:15 | [[#3. HTML: The Content]] | Steps 1–3 |
| 0:35 | [[#4. CSS: The Style]] | Steps 4–9 |
| 0:55 | [[#5. Make It Yours]] | Free time + challenges |
| 0:60 | [[#6. Put It Online (Optional)]] | |
| 0:75 | [[#7. Wrap-Up]] | |

> [!tip] If you're running behind
> Cut Section 5 down to 2 minutes ("here are some challenges to try at home") and make Section 6 homework. The cheat sheet has the publishing steps.

---

## ✅ Before the Meeting

### About a week before
- [ ] Send the [[#Pre-meeting message]] below
- [ ] Find 1–2 helpers who know a little HTML to walk around the room. Aim for about 1 helper per 8 people.
- [ ] If anyone will use school or lab computers, test one: can you install VS Code? Can you download and unzip files?

### The day before
- [ ] Zip `linktree-starter` (Windows: right-click → *Compress to ZIP file*; Mac: right-click → *Compress*)
- [ ] Upload the zip somewhere easy to reach (Google Drive, Discord, GitHub) and make a short link and a QR code for the projector
- [ ] Paste the link and QR code into the dashed box on slide 6 of `Link-Me Slides.pptx`
- [ ] Export [[Member Cheat Sheet]] to PDF (`Ctrl/Cmd + P` → *Export to PDF*) and share or print it
- [ ] Publish `linktree-finished` yourself (see [[#6. Put It Online (Optional)]]) so the hook can show a real, live URL
- [ ] Do a full, timed run-through by yourself, typing the code as you go

### Right before you start
- [ ] VS Code font size turned up (`Ctrl + =` / `Cmd + =` a few times). The back row needs to be able to read it.
- [ ] Browser zoom at 150% or higher
- [ ] VS Code and the browser side by side (Windows: `Win + ←/→`; Mac: hover the green window button)
- [ ] Notifications off / Do Not Disturb on
- [ ] Projector and adapter tested
- [ ] Download link and QR code ready to show
- [ ] These notes open on a second screen or your phone
- [ ] A fresh copy of `linktree-starter` to live-code in, so you're typing along with everyone

### Pre-meeting message
```
Hey everyone! 👋 At our next meeting we're building our own personal
"Linktree" website from scratch. No experience needed!

Please bring a charged laptop and, if you can, do this beforehand:
1. Install VS Code (free): https://code.visualstudio.com
2. Make sure you have Chrome, Edge, or Firefox
3. (Optional) Make a free GitHub account: https://github.com/signup
   We'll use it to put your site on the internet.
4. (Optional) Have a photo ready for your profile picture
   (you, your pet, a meme... anything works)

No laptop? Come anyway and pair up with someone!
```

---

## 1. Hook & Intro
*~5 min*

> [!example] Do
> Show your live published `linktree-finished` page on the projector. Hover over the buttons and click a link.

> [!quote] Say
> "By the end of today, you'll have one of these, and you'll have built it yourself. It's one page with all your links: GitHub, LinkedIn, Instagram, whatever you want. Sites like Linktree charge for the fancy version. We're going to build it from scratch with two languages: **HTML** and **CSS**."

### HTML vs. CSS: the house analogy

> [!quote] Say
> "Every website you've ever visited is built from three languages. Think of a house:
> - **HTML** is the *structure*: the walls, doors, and rooms. It says **what** is on the page.
> - **CSS** is the *paint and decoration*. It says how things **look**.
> - **JavaScript** is the *electricity*. It makes things **do** stuff. We don't need it today."

> [!example] Do: the magic trick (30 seconds, very effective)
> 1. In `linktree-finished/index.html`, delete the `<link rel="stylesheet" href="style.css">` line, save, and refresh. The page is now plain and ugly.
> 2. Undo (`Ctrl/Cmd + Z`), save, and refresh. It's pretty again.
>
> "Same HTML, same content. The only difference is the CSS."

> [!example] Optional: "every website is just HTML" (1 min)
> Go to any news site, right-click a headline → **Inspect**, double-click the text in the Elements panel, and change it to something silly. "You didn't hack anything, this only changed on your screen. But it shows that every website is HTML you can look at."

---

## 2. Setup
*~10 min*

> [!example] Do
> Put the download link and QR code on the projector.

### Step A: Download and unzip

> [!warning] Watch out: the #1 setup problem
> **Windows:** double-clicking a zip only lets you *peek* inside it. Edits won't save properly. You have to **right-click → Extract All**.
> **Mac:** double-clicking the zip extracts it automatically. That's fine.
>
> Tell people to extract to the **Desktop** so they can find it again.

### Step B: Open the folder in VS Code
1. Open VS Code → **File → Open Folder** → pick `linktree-starter`
2. If it asks *"Do you trust the authors?"*, click **Yes**
3. Click `index.html` in the left sidebar

> [!warning] Not using VS Code?
> - **Windows:** Notepad works fine (right-click the file → *Open with* → Notepad)
> - **Mac:** TextEdit **only** in plain-text mode (*Format → Make Plain Text*). Otherwise it quietly breaks the file.
> - **Chromebook / can't install anything:** see [[#🛟 Troubleshooting]]

### Step C: Open the page in a browser
Find `index.html` in File Explorer or Finder and **double-click** it (or drag it into a browser window).

> [!quote] Say
> "Look at the address bar. It starts with `file:///`. That means this page lives on **your computer**, and only you can see it right now. We'll put it on the internet at the end."

### The golden loop ✨

> [!important] Write this on the board and leave it up all session
> **Edit → Save → Refresh**
> - Save: `Ctrl + S` (Windows) / `Cmd + S` (Mac)
> - Refresh: `F5` or `Ctrl + R` (Windows) / `Cmd + R` (Mac)

> [!quote] Say
> "Almost every 'it's not working!' today will be because someone forgot to save or forgot to refresh. In VS Code, a **white dot** on the file's tab means you haven't saved yet."

> [!tip]
> Optional: turn on **File → Auto Save** in VS Code so saving happens on its own. You still have to refresh the browser.

> [!check] Checkpoint
> "Give me a thumbs up when you can see the page in your browser."
> Wait until most of the room is ready. Helpers can deal with the rest.

---

## 3. HTML: The Content
*~20 min*

### Anatomy of a tag

> [!example] Do
> Write this big on the projector or board:
> ```html
> <h1>Your Name</h1>
> ```

> [!quote] Say
> "HTML is made of **tags**. They're like labels on boxes. This one says *'this box is a heading.'*
> - `<h1>` is the **opening tag**
> - `</h1>` is the **closing tag**. Notice the slash.
> - Whatever is between them is the **content**."

The tags we use today:

| Tag | Stands for | What it does |
| --- | --- | --- |
| `<h1>` | heading 1 | The biggest heading |
| `<p>` | paragraph | A block of text |
| `<a>` | anchor | A link |
| `<img>` | image | A picture |

> [!example] Do: a quick tour of `index.html`
> Scroll through the file slowly from top to bottom:
> - **Gray text** is comments: `<!-- notes for humans -->`. The browser ignores them.
> - **`<head>`** is info *about* the page. "This is boilerplate, almost every site has it. Don't worry about it."
> - **`<body>`** is everything you can *see*. "This is where we'll work."
> - **The ✏️ comments** mark the spots you'll edit.

### Step 1: Your name and bio

> [!example] Do
> 1. Change `Your Name` in the `<h1>` to your name
> 2. Change the text in the `<p class="bio">` to a short bio
> 3. Change the `<title>` in the `<head>` too
> 4. **Save → Refresh.** Point out that the browser tab changed too.

> [!warning] Watch out
> People accidentally delete the `<` or `>` or the closing tag. Tell them: "Only change the text **between** the tags."

### Step 2: Your links

```html
<a class="link" href="https://github.com">💻 GitHub</a>
```

> [!quote] Say
> - "`href` means *where the link goes*. It's an **attribute**: extra info that lives inside the opening tag, written as `name="value"`."
> - "The text between the tags, `💻 GitHub`, is what people **see**."
> - "`class="link"` is like a **name tag**. It doesn't do anything yet, but we'll use it with CSS to style all the links at once."

> [!example] Do
> 1. Change a URL to your real profile, e.g. `https://github.com/yourusername`
> 2. Delete a link you don't need (delete the **whole line**)
> 3. **Add a link:** copy a whole line, paste it underneath, and change it
> 4. Save → Refresh → click the links to make sure they work

> [!tip] Link ideas
> GitHub, LinkedIn, Instagram, a Spotify playlist, YouTube, a portfolio, a club website.
> **Email:** `href="mailto:you@example.com"` opens the visitor's email app.
> **Emoji keyboard:** `Win + .` (Windows) / `Ctrl + Cmd + Space` (Mac)

> [!warning] Watch out
> - URLs **must** start with `https://`. Without it, the browser looks for a file on your computer and shows an error.
> - Keep both `"` quotes around the URL.
> - If the whole page suddenly turns into a link, someone deleted a `</a>`.

### Step 3: Your profile picture

```html
<img class="avatar" src="profile.svg" alt="Profile picture">
```

> [!quote] Say
> - "`<img>` has **no closing tag**, because nothing goes *inside* an image."
> - "`src` means *source*: which image file to show."
> - "`alt` is a description of the image. Screen readers read it out loud for blind users, and it shows up if the image fails to load. Always include it."

> [!example] Do
> 1. Copy your photo **into** the `linktree-starter` folder (next to `index.html`)
> 2. Change `src="profile.svg"` to your file's exact name, e.g. `src="me.jpg"`
> 3. Save → Refresh

> [!warning] Watch out: images are the #2 problem of the day
> - The name has to match **exactly**, including capital letters and the extension: `Me.JPG` ≠ `me.jpg`
> - **Windows hides file extensions.** Turn them on: File Explorer → *View → Show → File name extensions*. This is also why people end up with `me.jpg.jpg`.
> - **iPhone photos are often `.HEIC`**, which most browsers can't show. Convert it to JPG, or just take a screenshot of the photo.
> - Avoid spaces in file names (`my photo.jpg` → `my-photo.jpg`)
> - No photo? Keep `profile.svg`, or right-click any image online → *Copy image address* and paste that URL into `src`.

> [!quote] Say
> "Is your picture **enormous**? Perfect, that's expected. HTML doesn't know how big things should be. That's CSS's job, and it's next."

> [!check] Checkpoint
> "Everything on your page is now **your** content. HTML: done. ✅ Now let's make it look good."

---

## 4. CSS: The Style
*~20 min*

> [!example] Do
> Switch to `style.css`. Point out the comment at the top and the empty `STEP` sections: "We'll fill these in one at a time."

### Anatomy of a CSS rule

```css
body {
  background-color: black;
}
```

> [!quote] Say
> "Every CSS rule has three parts:
> - The **selector** (`body`) says **who** gets styled
> - The **property** (`background-color`) says **what** to change
> - The **value** (`black`) says **what to change it to**
>
> Curly braces `{ }` wrap the rule. A colon `:` goes between the property and the value. A semicolon `;` goes at the end of every line."

> [!quote] Say: classes
> "Remember the `class="link"` name tags from the HTML? In CSS, **a dot plus the class name** means *'everything wearing that name tag'*. So `.link` styles every link. No dot, like `body`, means *'this kind of tag'*."

> [!tip] How to run every step below
> 1. Explain what the step does
> 2. Type it live while they type along. **Encourage typing instead of copy-pasting**, because that's how it sticks. Copying is fine for anyone who's behind.
> 3. Save → Refresh → enjoy the change
> 4. Have them **change one value** to see what it does (each step has a suggestion)

### Step 4: Style the whole page

```css
body {
  background-color: #1e1e2e;
  color: white;
  font-family: Arial, sans-serif;
  text-align: center;
  padding: 40px 20px;
}
```

> [!quote] Say
> - `background-color`: "`#1e1e2e` is a **hex color**: a `#` and 6 characters. You can also use plain names like `hotpink` or `navy`."
> - `color`: "The **text** color. It isn't called `text-color`, CSS is a little weird like that."
> - `font-family`: "Use Arial, and if the computer doesn't have it, any sans-serif font."
> - `text-align: center`: centers everything
> - `padding: 40px 20px`: "Space around the edge of the page: 40 pixels top and bottom, 20 left and right."

> [!tip] Show this off
> In VS Code, a small **color square** shows up next to every color. Hover over it or click it to get a **color picker**. People love this.
> **Try it:** change the background to `hotpink`.

### Step 5: Make the profile picture round

```css
.avatar {
  width: 120px;
  height: 120px;
  border-radius: 50%;
  object-fit: cover;
  border: 4px solid white;
}
```

> [!quote] Say
> - `width` / `height`: "`px` means pixels, the tiny dots on your screen."
> - `border-radius: 50%`: "This rounds the corners. At 50% it rounds all the way into a circle."
> - `object-fit: cover`: "Crop the photo to fit instead of squishing it."
> - `border`: "A border, written as **thickness, style, color**."

> [!tip] Try it
> Change `border-radius` to `20px` to get a rounded square. Try `dashed` instead of `solid`.

### Step 6: Turn the links into buttons

```css
.link {
  display: block;
  background-color: #89b4fa;
  color: #1e1e2e;
  padding: 16px;
  margin-bottom: 12px;
  border-radius: 12px;
  text-decoration: none;
  font-weight: bold;
}
```

> [!quote] Say
> - `display: block`: "By default, links are **inline**. They sit side by side like words in a sentence. `block` makes each one take up a full row of its own, like a brick."
> - `text-decoration: none`: removes the underline
> - **padding vs. margin**, which comes up all the time:

> [!example] Do: draw this on the board
> ```
>         margin  (space OUTSIDE, between boxes)
>     ┌───────────────────────────┐
>     │   padding (space INSIDE)  │
>     │        💻 GitHub          │
>     └───────────────────────────┘
>         margin
> ```
> "**Padding** is the bubble wrap *inside* the box. **Margin** is the personal space *outside* it."

> [!example] Do
> Refresh with your browser window **full width**. The buttons stretch across the whole screen.
> "Uh oh. That looks weird on a laptop. Let's fix it."

### Step 7: Stop everything from getting too wide

```css
.card {
  max-width: 400px;
  margin: 0 auto;
}
```

> [!quote] Say
> - `max-width: 400px`: "**Never** wider than 400 pixels. It can still shrink on a small phone screen."
> - `margin: 0 auto`: "0 on the top and bottom. `auto` on the left and right means *split the leftover space evenly*, which centers it."

> [!example] Do
> Drag the browser window narrower and wider. It looks good at every size.

### Step 8: Add a hover effect

```css
.link:hover {
  background-color: #f5c2e7;
  transform: scale(1.05);
}
```

> [!quote] Say
> - `:hover`: "These styles **only** apply while the mouse is over the link."
> - `transform: scale(1.05)`: "Grow to 105% of the normal size."

> [!example] Do: the transition, part two
> Hover a few times. The change is instant and a bit choppy. Now **go back up to `.link`** and add one more line inside it:
> ```css
>   transition: 0.2s;
> ```
> Save → Refresh → hover again. "Now it animates smoothly over 0.2 seconds."
>
> This is also a good moment to show that you can go back and **add to an existing rule**.

### Step 9: Finishing touches

```css
.bio {
  color: #bac2de;
}

footer {
  margin-top: 40px;
  font-size: 14px;
  color: #6c7086;
}
```

> [!quote] Say
> "Small details like a softer bio color and a quieter footer are what make a design look polished."

> [!check] Checkpoint
> "Compare yours to mine. If it looks about the same, **congratulations, you just built a website.** 🎉"
> Anyone who's stuck can copy `style.css` from `linktree-finished` and keep going.

### Bonus: DevTools (about 3 min, highly recommended)

> [!example] Do
> 1. Right-click your page → **Inspect**
> 2. Click a link in the Elements panel. Its CSS shows up in the **Styles** panel.
> 3. Click a color value and change it live
> 4. Click the **phone/tablet icon** (`Ctrl + Shift + M` / `Cmd + Shift + M`) to see the page at phone size
>
> "This is how professionals experiment: try things in DevTools, then copy what you like back into your file. **Changes here disappear when you refresh.**"
> "And most people open a linktree on their phone. Ours already works there, thanks to `max-width`."

---

## 5. Make It Yours
*~5–15 min, free time while you and the helpers walk around*

> [!quote] Say
> "Now make it **yours**. Change colors, fonts, anything. Here are some challenges if you want ideas."

> [!example] Do
> Put this list on the projector. The snippets are in the [[Member Cheat Sheet]] too.

> [!success]- 🟢 Easy: your own color palette
> Use [coolors.co](https://coolors.co) to generate a palette, then swap out every hex code.

> [!success]- 🟢 Easy: a different font
> ```css
> font-family: "Courier New", monospace;   /* hacker vibes */
> font-family: Georgia, serif;             /* fancy */
> font-family: "Comic Sans MS", cursive;   /* chaos */
> ```

> [!success]- 🟢 Easy: shadows on the buttons
> Add to `.link`:
> ```css
> box-shadow: 0 4px 12px rgba(0, 0, 0, 0.4);
> ```

> [!warning]- 🟡 Medium: a gradient background
> Replace `background-color` in `body` with:
> ```css
> background: linear-gradient(135deg, #1e1e2e, #45475a);
> background-attachment: fixed;
> ```
> (`background-attachment: fixed` stretches the gradient to fill the window so it doesn't repeat in stripes.)

> [!warning]- 🟡 Medium: open links in a new tab
> Add `target="_blank"` to each link:
> ```html
> <a class="link" href="https://github.com" target="_blank">💻 GitHub</a>
> ```

> [!warning]- 🟡 Medium: a tab icon (favicon)
> Add this inside `<head>`:
> ```html
> <link rel="icon" href="profile.svg">
> ```

> [!warning]- 🟡 Medium: a Google Font
> 1. Go to [fonts.google.com](https://fonts.google.com) and pick a font
> 2. Click **Get font → Get embed code**
> 3. Paste the `<link>` tags into your `<head>`, **above** your `style.css` link
> 4. Copy the `font-family` line into your `body` rule

> [!danger]- 🔴 Hard: outline-style buttons
> Make `.link` transparent with a colored border, then fill it in on hover:
> ```css
> .link {
>   background-color: transparent;
>   border: 2px solid #89b4fa;
>   color: #89b4fa;
> }
>
> .link:hover {
>   background-color: #89b4fa;
>   color: #1e1e2e;
> }
> ```

> [!danger]- 🔴 Hard: group your links into sections
> Add `<h2>Socials</h2>` and `<h2>Projects</h2>` between groups of links in the HTML, then style `h2` in CSS. Try making the headings small, all caps (`text-transform: uppercase;`), and spaced out (`letter-spacing: 2px;`).

> [!danger]- 🔴 Hard: real brand icons
> Look up **Font Awesome** or **Simple Icons** and get real GitHub/LinkedIn logos working in place of the emoji. This means reading documentation, which is a real developer skill.

---

## 6. Put It Online (Optional)
*~15 min. Do this in the meeting if you have time, otherwise make it homework.*

> [!warning] Say this first: privacy
> "Once this is online, **anyone** can see it. Don't put your phone number, home address, or anything you wouldn't put on a poster in the hallway."

### GitHub Pages (free, no installs, all in the browser)

1. Sign in at [github.com](https://github.com)
2. Click **+** (top right) → **New repository**
3. **Repository name:** `YOUR-USERNAME.github.io`, using your actual GitHub username (lowercase) → **Public** → **Create repository**
4. On the new repo page, click the **"uploading an existing file"** link
5. Drag in the **files**: `index.html`, `style.css`, and your photo. Drag the files themselves, **not the folder**.
6. Click **Commit changes**
7. Go to **Settings → Pages**. Under *Build and deployment*, check that the source is **Deploy from a branch** with branch **main** and **/ (root)**. If it isn't, set it and click **Save**.
8. Wait 1–2 minutes, then visit **`https://YOUR-USERNAME.github.io`** 🎉

> [!warning] Watch out
> - The file **must** be named `index.html` in lowercase. It's the page web servers show by default.
> - If you dragged in the folder, the site ends up at `.../linktree-starter/`. Delete it and upload just the files.
> - Updates take a minute or two to show up. Force-refresh with `Ctrl + Shift + R` / `Cmd + Shift + R`.
> - The repo name has to match the username **exactly**, or the URL won't work.

> [!tip] Updating the site later
> In the repo, click a file → the **pencil icon** to edit it in the browser. Or use **Add file → Upload files** to replace it.

> [!note] Alternative: Netlify Drop
> [app.netlify.com/drop](https://app.netlify.com/drop): drag the whole folder in and it's live in seconds. You need a free account to keep it online, though.

> [!quote] Say
> "Copy that URL and paste it into your Instagram, TikTok, or LinkedIn bio. It's real, it's live, and you built it."

---

## 7. Wrap-Up
*~5 min*

> [!quote] Say
> "Today you wrote HTML and CSS, the same languages behind every website you've ever visited. Google, YouTube, Instagram: all HTML and CSS underneath. You're not 'learning to code someday' anymore. You did it today."

- **Show and tell:** ask for 2–3 volunteers to share their page on the projector (always ask first)
- **Share links:** have everyone post their URL in the club Discord or group chat
- **Where to learn more:**
  - [MDN Web Docs](https://developer.mozilla.org): *the* reference for HTML and CSS
  - [freeCodeCamp](https://www.freecodecamp.org): free, guided, beginner-friendly courses
  - [Flexbox Froggy](https://flexboxfroggy.com): learn CSS layout by playing a game
  - [web.dev/learn/css](https://web.dev/learn/css): deeper CSS lessons
- **Tease the next workshop:** "Next time: **JavaScript**, so we can make things *do* stuff, like a dark-mode toggle button."
- **Get feedback:** a quick poll or a show of hands: *"What was the most confusing part?"* Use the answers to improve the next session.

---

## 🛟 Troubleshooting

> [!faq]- "My changes aren't showing up"
> 1. Did you **save**? Look for a white dot on the VS Code tab.
> 2. Did you **refresh** the browser?
> 3. Are you editing the **same file** the browser is showing? Compare the browser's address bar with the file path in VS Code. A common cause is editing a copy inside the zip, or having two copies of the folder.

> [!faq]- "My page has no styling at all"
> - `style.css` has to be in the **same folder** as `index.html`
> - The file name has to be exactly `style.css`. Watch for `style.css.txt` (turn on file extensions in Windows).
> - The `<link rel="stylesheet" href="style.css">` line must still be in the `<head>`

> [!faq]- "Some of my CSS works, but everything after a certain point is broken"
> There's a missing `}`, `:`, or `;` **just above** the first rule that stopped working. VS Code underlines errors with a red squiggle.

> [!faq]- "My image shows a broken icon"
> - The file name doesn't match exactly (capital letters, extension, spaces)
> - The photo isn't in the same folder as `index.html`
> - It's an iPhone `.HEIC` file. Convert it to JPG or take a screenshot of it.
> - The file is really `me.jpg.jpg` (turn on file extensions in Windows)

> [!faq]- "Clicking my link gives a 'file not found' error"
> The URL is missing `https://` at the start.

> [!faq]- "Everything after a certain point turned into a link (blue and underlined)"
> A closing `</a>` is missing.

> [!faq]- "Emoji show up as weird symbols like ðŸ’»"
> The `<meta charset="UTF-8">` line got deleted, or the file was saved in a different encoding. In VS Code, check the bottom-right corner: it should say **UTF-8**.

> [!faq]- "VS Code says Restricted Mode"
> Click **Trust** / **Yes, I trust the authors**.

> [!faq]- "On my Mac, index.html opens in TextEdit or Xcode instead of a browser"
> Right-click → **Open With** → Chrome or Safari.

> [!faq]- "I'm on a Chromebook / I can't install anything"
> Use [codepen.io](https://codepen.io) in the browser:
> - Paste the HTML that's **inside `<body>`** into the HTML panel
> - Paste the CSS into the CSS panel
> - Use an image **URL** for the profile picture instead of a file
> - Make a free account to save your work
> Or pair them up with someone who has a laptop.

> [!faq]- "I messed it up so badly I want to start over"
> Re-download the starter zip, or copy the files from `linktree-finished` and change the content to your own.

---

## 🙋 Questions You Might Get

> [!question]- "Why not just use Linktree or Wix?"
> You can! But building it yourself means it's free, you can customize **everything**, and you've learned a real skill. This is also how every website builder works under the hood.

> [!question]- "Do I have to memorize all of this?"
> No. Professional developers look things up constantly. What matters is knowing what's *possible* and how to search for it. "How to make rounded corners CSS" is a totally normal thing to Google.

> [!question]- "Is HTML a programming language?"
> Technically no. It's a **markup** language: it describes content but doesn't make decisions or do math. CSS is a **styling** language. JavaScript is the programming language of the web.

> [!question]- "What's the difference between `class` and `id`?"
> A `class` can be used on as many elements as you like (all of our links share `class="link"`). An `id` should be unique: one per page. In CSS, a class is `.name` and an id is `#name`.

> [!question]- "Why is the file called `index.html`?"
> When you visit a website without naming a specific page, the server automatically shows the file called `index.html`. That's why it matters for publishing.

> [!question]- "What's `<!DOCTYPE html>` / `<meta>` / `viewport`?"
> Boilerplate. `DOCTYPE` tells the browser "this is modern HTML". `charset` makes emoji and special characters display correctly. `viewport` makes the page look right on phones. You copy these into every page and stop thinking about them.

> [!question]- "Can I make it do things when I click, like a dark-mode button?"
> That's JavaScript, and it's coming next workshop. 😉
