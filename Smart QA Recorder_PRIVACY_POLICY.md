# Privacy Policy for Smart QA Recorder

**Effective Date:** November 17, 2026

Smart QA Recorder ("the Extension") is a developer and QA productivity tool designed to help testers capture bug context and submit issue tickets to their configured WireWork (Jira) instance.

## 1. Data We Collect and Process

The Extension only collects data when the user explicitly activates recording ("Start") or triggers a capture ("Capture"):

- **Website Content & Technical Context:** Console logs (`error`, `warn`, `info`, `debug`), uncaught page errors, browser/OS environment metadata, screenshots of the active tab, and (when enabled by the user) a temporary rolling video recording of the active tab.
- **User Activity (Network Metadata):** HTTP method, redacted URL, status code, duration, and error state of network requests on the tab under test. Request and response bodies are not collected by the network tracker.
- **Configuration & Credentials:** User settings (buffer duration, redaction keys, floating button position/visibility) and the user's WireWork personal access token.

## 2. How Data Is Used

All captured data is used **solely** to:
- Pre-fill a bug report form for the user to review and edit.
- Generate an offline HTML diagnostic report (`qa-report-*.html`) and optional video clip (`qa-clip-*.webm`) for attachment to the bug ticket.
- Submit the bug ticket and attachments to the WireWork server URL configured by the user, only after the user's explicit confirmation.

## 3. Data Redaction & Security

- Before storing logs or network metadata in memory or including them in a ticket/report, the Extension automatically strips sensitive headers (`Authorization`, `Cookie`, `Set-Cookie`) and redacts configured sensitive keys (such as `password`, `token`, `authorization`, `cookie`, `card`), email addresses, and card-number patterns.
- Your WireWork personal access token is stored locally in `chrome.storage.local` on your device and is only read by the Extension's background service worker to authenticate requests to your configured WireWork server.
- Rolling buffers (console, network, and video chunks) are kept only in local memory and are cleared when recording stops or the tab closes.

## 4. Data Sharing & Third Parties

- The Extension **does not** sell, rent, or transfer user data to any third parties, advertisers, or analytics services.
- Data never leaves your browser except when you explicitly submit a ticket to your configured WireWork server (`https://wire.lgcns.com/*` or your configured HTTPS endpoint).

## 5. User Control

You can disable console, network, screenshot, or video capture at any time in the Extension's Settings page, or remove your stored WireWork token and clear local settings.

## 6. Contact

If you have any questions about this Privacy Policy, please contact your internal QA/Engineering team or the Extension maintainer.
