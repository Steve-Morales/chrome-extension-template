# Chrome Extension File Structure

For complex Chrome extensions, the file structure should be organized to separate different components of the extension, making it easy to manage and navigate. Here’s a typical structure:

## 1. **Root Directory**
This is the top-level directory of your extension, containing essential files like `manifest.json`.

- **`manifest.json`**: The main configuration file for the Chrome extension.
- **`README.md`**: <u>**[Optional]**</u> useful for documentation.
- **`LICENSE`**: <u>**[Optional]**</u> If your extension is open-source

## 2. **`src` or `app` Directory**
This directory holds all the source code for your extension. It's often divided into subdirectories based on functionality.

- **`background/`**: Contains background scripts or the service worker.
  - `background.js` or `service-worker.js`
  
- **`content/`**: Contains content scripts that interact with web pages.
  - `content.js`
  - Additional files for handling specific content script tasks, if needed.

- **`popup/`**: Contains the HTML, CSS, and JS files for the popup UI.
  - `popup.html`
  - `popup.js`
  - `popup.css`

- **`options/`**: Contains files for the options page, where users can configure the extension.
  - `options.html`
  - `options.js`
  - `options.css`

- **`scripts/`**: Utility or shared scripts that are used across different components.
  - `utils.js`

- **`pages/`**: HTML files for other pages, like background pages, or any other UI your extension might need.
  - `background.html`
  - Other custom pages

## 3. **`assets` or `resources` Directory**
This directory contains static assets like images, icons, fonts, and other resources.

- **`icons/`**
  - `icon16.png`
  - `icon48.png`
  - `icon128.png`

- **`images/`**: Other images used in the extension.

## 4. **`locales/` Directory**
This directory contains language files for localization.

- **`en/`**
  - `messages.json`
- **`es/`**
  - `messages.json`

## 5. **`styles/` Directory**
Contains global or shared CSS files.

- `common.css`

## 6. **`test/` Directory**
Contains test files for your extension.

- **`unit/`**: Unit tests
- **`integration/`**: Integration tests

## Example Structure:

```plaintext
my-extension/
│
├── manifest.json
├── README.md
├── LICENSE
│
├── src/
│   ├── background/
│   │   └── service-worker.js
│   │
│   ├── content/
│   │   └── content.js
│   │
│   ├── popup/
│   │   ├── popup.html
│   │   ├── popup.js
│   │   └── popup.css
│   │
│   ├── options/
│   │   ├── options.html
│   │   ├── options.js
│   │   └── options.css
│   │
│   ├── scripts/
│   │   └── utils.js
│   │
│   ├── pages/
│   │   └── background.html
│   │
│   └── styles/
│       └── common.css
│
├── assets/
│   ├── icons/
│   │   ├── icon16.png
│   │   ├── icon48.png
│   │   └── icon128.png
│   └── images/
│       └── logo.png
│
├── locales/
│   ├── en/
│   │   └── messages.json
│   └── es/
│       └── messages.json
│
└── test/
    ├── unit/
    │   └── content.test.js
    └── integration/
        └── popup.test.js
```