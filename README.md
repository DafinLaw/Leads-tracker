# Chrome Lead Saver Extension

A lightweight Chrome extension that allows users to quickly save URLs (leads) either manually or directly from the currently active browser tab. All data is persisted locally, so saved links remain available across browser sessions.

Live Demo: https://dafinlaw.github.io/Leads-tracker/

---

## Features

- Save the current active tab URL with one click
- Manually add custom URLs
- Persistent storage using `localStorage`
- Clickable links that open in a new tab
- Intentional delete action (double-click) to prevent accidental data loss
- Simple, clean UI focused on usability

---

## Why This Project

This project was built to better understand:
- State management in JavaScript
- Data persistence in browser-based applications
- DOM rendering based on application state
- Interaction with browser APIs (Chrome Tabs API)
- UX-conscious design decisions in small tools

The extension mirrors real-world application behavior in a simplified form.

---

## Tech Stack

- JavaScript (ES6+)
- HTML
- CSS
- Chrome Extension APIs
- `localStorage` for persistence

---

## How It Works (High Level)

- The application maintains a single source of truth (`myLeads`)
- All UI updates are generated from this state via a dedicated render function
- User actions update state → persist to `localStorage` → re-render UI
- On load, stored data is rehydrated from `localStorage`

---

## Installation (Developer Mode)

Since this extension is not published on the Chrome Web Store, it must be loaded manually:

1. Clone or download this repository:
   ```bash
   git clone https://github.com/DafinLaw/your-repo-name.git
2. Open Google Chrome and navigate to: chrome://extensions
3. Enable Developer mode (top-right corner)
4. Click Load unpacked
5. Select the project folder (the one containing manifest.json)
6. The extension will now appear in your extensions list and be ready to use

Usage

- Click Save Tab to store the current active tab URL

- Enter a URL manually and click Save Input

- Double-click Delete All to clear stored leads

- Click any saved link to open it in a new tab


Future Improvements

- Automatic extension updates

- UI/UX refinements

- Validation for input URLs

- Sync storage option

Notes on Updates

Currently, updates require reloading the extension manually in chrome://extensions.
Automatic updates would require:

- Publishing the extension to the Chrome Web Store, or

- Hosting an update manifest and versioned release system

This is planned for a future iteration

License

This project is for learning and demonstration purposes.
