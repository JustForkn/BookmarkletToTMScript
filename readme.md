# `BOOKMARKLET → TAMPERMONKEY`

```text
██████╗  ██████╗  ██████╗ ██╗  ██╗███╗   ███╗ █████╗ ██████╗ ██╗  ██╗███████╗████████╗
██╔══██╗██╔═══██╗██╔═══██╗██║ ██╔╝████╗ ████║██╔══██╗██╔══██╗██║ ██╔╝██╔════╝╚══██╔══╝
██████╔╝██║   ██║██║   ██║█████╔╝ ██╔████╔██║███████║██████╔╝█████╔╝ █████╗     ██║
██╔══██╗██║   ██║██║   ██║██╔═██╗ ██║╚██╔╝██║██╔══██║██╔══██╗██╔═██╗ ██╔══╝     ██║
██████╔╝╚██████╔╝╚██████╔╝██║  ██╗██║ ╚═╝ ██║██║  ██║██║  ██║██║  ██╗███████╗   ██║
╚═════╝  ╚═════╝  ╚═════╝ ╚═╝  ╚═╝╚═╝     ╚═╝╚═╝  ╚═╝╚═╝  ╚═╝╚═╝  ╚═╝╚══════╝   ╚═╝
```

<p align="center">
  <strong>Convert JavaScript bookmarklets into ready-to-use Tampermonkey userscripts.</strong>
</p>

<p align="center">
  <a href="#-features">Features</a> •
  <a href="#-demo">Demo</a> •
  <a href="#-usage">Usage</a> •
  <a href="#-screenshots">Screenshots</a> •
  <a href="#-installation">Installation</a>
</p>

---

## 🏷️ Badges

<p align="center">

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge\&logo=html5\&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge\&logo=css3\&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge\&logo=javascript\&logoColor=black)
![Tampermonkey](https://img.shields.io/badge/Tampermonkey-00485B?style=for-the-badge)
![No Backend](https://img.shields.io/badge/Backend-None-success?style=for-the-badge)
![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-Compatible-222?style=for-the-badge\&logo=github)

</p>

---

## 🚀 What Is This?

**Bookmarklet → Tampermonkey** is a lightweight browser-based converter that turns JavaScript bookmarklets into properly formatted Tampermonkey userscripts.

Instead of manually creating userscript metadata every time, paste your bookmarklet, configure the script, and generate a ready-to-install `.user.js` file.

### The basic idea

```text
┌─────────────────────┐
│   JavaScript        │
│    Bookmarklet      │
└──────────┬──────────┘
           │
           ▼
    ┌─────────────┐
    │   CONVERTER │
    └──────┬──────┘
           │
           ▼
┌─────────────────────┐
│ Tampermonkey        │
│ Userscript          │
│     (.user.js)      │
└─────────────────────┘
```

No server.
No database.
No complicated setup.

Just **paste → configure → convert → install**.

---

# ✨ Features

| Feature                   | Description                                                 |
| ------------------------- | ----------------------------------------------------------- |
| 🔄 Bookmarklet Conversion | Converts JavaScript bookmarklets into userscripts           |
| 🧹 Auto Prefix Removal    | Automatically handles the `javascript:` prefix              |
| 📝 Custom Metadata        | Configure name, author, version, description, and namespace |
| 🌐 Custom `@match`        | Choose exactly which websites the script should run on      |
| 🔐 Grant Support          | Add Tampermonkey `@grant` permissions                       |
| 👀 Live Preview           | Preview the generated userscript before exporting           |
| 📋 Copy to Clipboard      | Copy the complete userscript instantly                      |
| 💾 `.user.js` Export      | Download your converted script                              |
| ⚡ Browser-Based           | Everything happens locally in your browser                  |
| 📴 No Backend             | No server required                                          |
| 📱 Responsive UI          | Works across desktop and supported mobile browsers          |
| 🌙 Modern Interface       | Clean, modern interface designed for quick conversions      |

---

# 🎬 Demo

### Convert a bookmarklet

Start with something like:

```javascript
javascript:(()=>{alert("Hello from my bookmarklet!");})();
```

Configure your userscript:

```text
Name:        Hello Bookmarklet
Namespace:   https://example.com/
Version:     1.0.0
Author:      Your Name
Match:       https://example.com/*
Grant:       none
```

Then generate:

```javascript
// ==UserScript==
// @name         Hello Bookmarklet
// @namespace    https://example.com/
// @version      1.0.0
// @description  Converted bookmarklet
// @author       Your Name
// @match        https://example.com/*
// @grant        none
// ==/UserScript==

(() => {
    alert("Hello from my bookmarklet!");
})();
```

Download it as:

```text
hello-bookmarklet.user.js
```

Then import it into Tampermonkey.

---

# 🖼️ Screenshots

> Replace the placeholders below with screenshots of your actual converter.

### Main Converter

```text
┌──────────────────────────────────────────────────────────┐
│                                                          │
│        🔄 BOOKMARKLET → TAMPERMONKEY                     │
│                                                          │
│   Convert bookmarklets into userscripts instantly.       │
│                                                          │
│  ┌────────────────────────────────────────────────────┐  │
│  │ Paste your bookmarklet here...                     │  │
│  │                                                    │  │
│  │ javascript:(()=>{ ... })();                        │  │
│  │                                                    │  │
│  └────────────────────────────────────────────────────┘  │
│                                                          │
│  Script Name     Version       Author                    │
│  ┌───────────┐   ┌─────────┐   ┌────────────────────┐   │
│  │ My Script │   │ 1.0.0   │   │ Your Name          │   │
│  └───────────┘   └─────────┘   └────────────────────┘   │
│                                                          │
│                 [ ⚡ CONVERT ]                           │
│                                                          │
└──────────────────────────────────────────────────────────┘
```

### Generated Userscript

```text
┌──────────────────────────────────────────────────────────┐
│ Generated Userscript                         [ COPY ]    │
├──────────────────────────────────────────────────────────┤
│ // ==UserScript==                                        │
│ // @name         My Script                              │
│ // @version      1.0.0                                  │
│ // @match        *://*/*                                │
│ // @grant        none                                   │
│ // ==/UserScript==                                       │
│                                                          │
│ (() => {                                                 │
│     ...                                                  │
│ })();                                                    │
└──────────────────────────────────────────────────────────┘
```

### Recommended Screenshot Layout

When adding real screenshots to the repository:

```text
assets/
└── screenshots/
    ├── main.png
    ├── settings.png
    └── output.png
```

Then display them with:

```markdown
![Main Converter](assets/screenshots/main.png)

![Settings](assets/screenshots/settings.png)

![Generated Userscript](assets/screenshots/output.png)
```

---

# 📖 Usage

## 1. Paste Your Bookmarklet

Copy your bookmarklet and paste it into the converter.

Example:

```javascript
javascript:(function(){
    document.body.style.background = "black";
})();
```

The converter can automatically remove:

```text
javascript:
```

from the beginning.

---

## 2. Configure Your Script

Customize the generated metadata.

### Name

```text
My Custom Script
```

### Version

```text
1.0.0
```

### Author

```text
Your Name
```

### Match

```text
https://example.com/*
```

### Namespace

```text
https://example.com/
```

---

## 3. Generate

Click:

```text
⚡ CONVERT
```

The converter generates the complete Tampermonkey userscript.

---

## 4. Copy or Download

You can either:

```text
📋 COPY
```

or:

```text
💾 DOWNLOAD .USER.JS
```

---

# 🧩 Example

### Input

```javascript
javascript:(function(){
    document.body.style.backgroundColor = "black";
    document.body.style.color = "white";
})();
```

### Output

```javascript
// ==UserScript==
// @name         Dark Page
// @namespace    https://example.com/
// @version      1.0.0
// @description  Converted bookmarklet
// @author       Your Name
// @match        *://*/*
// @grant        none
// ==/UserScript==

(function(){
    document.body.style.backgroundColor = "black";
    document.body.style.color = "white";
})();
```

---

# 🌐 Understanding `@match`

The `@match` property tells Tampermonkey where your script can run.

### One website

```text
https://example.com/*
```

### A subdomain pattern

```text
https://*.example.com/*
```

### Most HTTP/HTTPS websites

```text
*://*/*
```

For security and performance, use the **narrowest pattern that works**.

---

# 🔐 Tampermonkey Permissions

Scripts that don't require Tampermonkey APIs can generally use:

```javascript
// @grant        none
```

Scripts that use Tampermonkey APIs may require additional grants.

For example:

```javascript
// @grant        GM_getValue
// @grant        GM_setValue
```

The converter can include these permissions in the generated metadata when needed.

> ⚠️ Only add permissions that your script actually requires.

---

# ⚠️ Compatibility

A bookmarklet and a userscript don't always execute in exactly the same environment.

Some bookmarklets may require manual changes if they depend on:

* Page-specific JavaScript variables
* Bookmarklet-specific URL behavior
* Dynamic script injection
* Cross-origin requests
* Browser APIs
* Special execution contexts
* External resources

This project primarily converts the **bookmarklet wrapper and userscript metadata**. It does not guarantee that every bookmarklet will work without modification.

---

# 🛠️ Technology

The project is intentionally lightweight.

```text
HTML
 ├── Interface
 └── Structure

CSS
 ├── Styling
 ├── Layout
 └── Responsive design

JavaScript
 ├── Bookmarklet parsing
 ├── Metadata generation
 ├── Preview
 ├── Clipboard support
 └── File generation
```

### No backend required

Everything happens locally:

```text
Your Browser
     │
     ├── Bookmarklet
     │
     ├── Converter
     │
     └── Generated Userscript
```

Your bookmarklet does not need to be uploaded to a server just to convert it.

---

# 📦 Installation

## Option 1 — Use the Website

Open the hosted version of the converter.

> Add your GitHub Pages URL here once the project is deployed.

---

## Option 2 — Run Locally

Clone the repository:

```bash
git clone https://github.com/YOUR_USERNAME/bookmarklet-to-tampermonkey.git
```

Enter the directory:

```bash
cd bookmarklet-to-tampermonkey
```

Then open:

```text
index.html
```

in your browser.

No Node.js installation is required if the project is fully client-side.

---

# 🌍 GitHub Pages

This project can be hosted using GitHub Pages.

### Setup

1. Open your repository.
2. Go to **Settings**.
3. Open **Pages**.
4. Select your main branch.
5. Select the repository root.
6. Save.
7. Wait for GitHub Pages to deploy.

Your converter will then be available through your GitHub Pages URL.

---

# 📁 Project Structure

```text
bookmarklet-to-tampermonkey/
│
├── index.html
├── README.md
├── LICENSE
│
└── assets/
    └── screenshots/
        ├── main.png
        ├── settings.png
        └── output.png
```

If the project is completely self-contained, `index.html` can contain the HTML, CSS, and JavaScript in one file.

---

# 🐛 Troubleshooting

## The generated script doesn't run

Check:

* Your `@match` pattern.
* Whether the original bookmarklet works.
* Whether the script requires additional permissions.
* Whether the website has restrictive security policies.
* The browser console for JavaScript errors.

---

## Tampermonkey doesn't detect the script

Make sure the file ends with:

```text
.user.js
```

For example:

```text
my-script.user.js
```

Also verify that Tampermonkey is enabled.

---

## The bookmarklet starts with `javascript:`

That's expected.

The converter should turn:

```javascript
javascript:alert("Hello");
```

into:

```javascript
alert("Hello");
```

before generating the userscript.

---

# 🔒 Privacy

The converter is designed to process bookmarklets **locally in your browser**.

There is no requirement for a backend to perform the conversion.

If you host your own copy, you can inspect the source code to verify exactly what the converter does.

---

# 🤝 Contributing

Contributions are welcome!

You can help by:

* 🐛 Reporting bugs
* 💡 Suggesting features
* 🎨 Improving the UI
* ⚡ Improving conversion performance
* 📚 Improving documentation
* 🔧 Fixing compatibility issues
* 🧪 Testing unusual bookmarklets

### Suggested workflow

```bash
git checkout -b feature/my-feature
```

Make your changes, test them, then submit a pull request.

---

# 🗺️ Roadmap

Potential future features:

* [ ] Drag-and-drop bookmarklet files
* [ ] Automatic script description detection
* [ ] Advanced `@grant` selector
* [ ] Automatic `@require` detection
* [ ] Multiple bookmarklet conversion
* [ ] Batch `.user.js` export
* [ ] Import existing userscripts
* [ ] Bookmarklet ↔ userscript conversion
* [ ] Syntax highlighting
* [ ] Error detection
* [ ] Minified bookmarklet support
* [ ] Conversion history
* [ ] Custom themes
* [ ] PWA/offline support

---

# ⭐ Support

If this project is useful, consider giving the repository a ⭐ on GitHub.

It helps the project get discovered by other people who need a quick bookmarklet converter.

---

# 📜 License

This project is available under the license included in the repository.

See [`LICENSE`](LICENSE) for details.

---

<div align="center">

## 🔄 Bookmarklet → Tampermonkey

**Paste it. Convert it. Install it.**

```text
JavaScript Bookmarklet
        ↓
     Converter
        ↓
Tampermonkey Userscript
        ↓
       Done ⚡
```

Made for people who don't want to manually write userscript headers every five seconds.

</div>
