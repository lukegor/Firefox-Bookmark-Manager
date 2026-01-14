# Bookmark Manager

A developer-centric tool for advanced bookmark management, cleanup, and analytics directly via the Firefox DevTools console.

> CLI/Console Mode

## 🚀 Overview

This extension provides a powerful interface for users who need to manage massive bookmark libraries (thousands of items) where the standard browser UI lags or lacks functionality. It operates in the background, indexing bookmarks by domain and allowing for bulk operations via JavaScript commands.

## ⚠️ Compatibility

Currently, this extension only supports Firefox. Chrome and other Chromium-based browsers are not supported at this time. **Note**: Manifest V3 is not supported.

## 🛠 Installation (Developer Mode)

1. Clone this repository.
2. Open Firefox and navigate to `about:debugging#/runtime/this-firefox`.
3. Click **"Load Temporary Add-on..."**.
4. Select the `manifest.json` file from the project directory.

## 💻 Usage

Once loaded, open the extension's background console (Inspect) and use the globally exposed API:

### 1. List & Analyze

Find domains with 1 to 50 bookmarks, filter for "google", and copy results to clipboard:

```javascript
// listByRangeCount(min, max, [filters], strictMode)
listByRangeCount(1, 50, ['google'], false);
```

## 📜 License

This project is licensed under the [Apache License 2.0](https://opensource.org/license/apache-2-0/)
