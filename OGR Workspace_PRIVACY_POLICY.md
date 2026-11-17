# Privacy Policy for OGR Workspace Companion

**Last updated:** November 17, 2026

OGR Workspace Companion ("the Extension") is an internal productivity browser extension developed for LG CNS Vietnam employees to access OGR Workspace features directly from their browser.

## 1. Information We Collect and Process

To provide its core functionality, the Extension processes the following data:
- **Authentication Information:** Your Employee ID (`empNo`), password (submitted directly to your configured OGR Workspace server only during login and never stored in plain text), and the resulting JWT authentication token.
- **Personally Identifiable Information:** Your employee number, name, role, and permissions retrieved from your OGR Workspace account. For authorized administrators or users with `/employee` permission, the Extension also displays employee directory details (employee ID, name, email, department, and employment status) fetched from the OGR Workspace server.
- **Workspace & Productivity Data:** Today's check-in/check-out records, My Work items, My Task items, and favorite menu links fetched from your configured OGR Workspace server.
- **User Preferences & Custom Links:** Extension settings (server URL, float button visibility and position, auto-refresh interval, saved filter preferences) and custom external favorite links that you explicitly add or save via the "+ Lưu tab này" action.

## 2. How We Use Information

All data is used strictly to:
- Authenticate your session with the OGR Workspace server you configure.
- Display your personal attendance, My Work, My Task, and favorite links in the extension popup, quick popover, and detail modal.
- Periodically refresh your dashboard data in the background according to your chosen interval.

## 3. Data Storage and Security

- All session tokens, settings, custom favorite links, and cached dashboard snapshots are stored **locally on your device** using `chrome.storage.local` (and `localStorage` for instant popup rendering).
- The Extension communicates **only** with the OGR Workspace server URL configured by you.
- Logging out immediately clears your stored session token and cached dashboard data.

## 4. Third-Party Sharing

- We do **not** sell, rent, or transfer your personal or authentication data to any third parties, advertisers, or analytics services.
- We do **not** track your browsing history or collect website content from pages you visit, except when you explicitly click "+ Lưu tab này" to save a page title and URL as your own favorite link.

## 5. Contact

If you have questions about this Privacy Policy or data handling, please contact the OGR Workspace administration team at LG CNS Vietnam.
