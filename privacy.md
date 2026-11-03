# SnippetShelf Privacy Policy

**Effective date:** 3 November 2026

SnippetShelf ("the Extension") is a browser extension for saving, organizing, copying, and discovering reusable text snippets and prompts. This policy explains what data the Extension handles and how.

## 1. Summary

SnippetShelf stores your snippets and folders locally in your browser. Analytics events are sent through our Vercel-hosted backend to Google Analytics and contain only a random pseudonymous client identifier, a session identifier, the event name, and numerical parameters. We do not send snippet contents, search queries, emails, passwords, authentication tokens, or IP addresses to Google Analytics. Community library searches are sent to our backend to filter results. Backup imports stay local to your browser.

## 2. Data Stored Locally on Your Device

- **Snippets and folders:** stored locally in your browser using IndexedDB. They are not transmitted to us.
- **Analytics identifiers:** a randomly generated client ID, a session ID, and a session timestamp, stored in `chrome.storage.local`. The client ID distinguishes your installation and the session ID groups interactions within a session. They stay on your device until the Extension's local data is removed, for example by uninstalling.
- **Interface settings:** panel position, size, zoom, and a close-on-outside-click preference, stored in `chrome.storage.local`.
- **Backups:** exporting and importing a backup is handled entirely in your browser. Backup contents are not sent to our backend or to Google Analytics.

Uninstalling the Extension removes this locally stored data from your browser.

## 3. Data Sent to Our Servers

**Analytics events.** The Extension sends usage events to our backend, hosted on Vercel, which forwards them to Google Analytics 4. Events include:

- Opening the extension
- Creating a snippet
- Copying a snippet
- Opening the community library
- Saving a community snippet
- Performing a library search

Each event contains only the random client identifier, the session identifier, the event name, and numerical parameters (such as engagement time). Events do **not** contain snippet contents, search terms, or personal information such as emails or passwords.

**About these identifiers.** The client and session identifiers are pseudonymous, not anonymous. They do not directly reveal your name or email address, but depending on where you live they may still be treated as personal data under privacy laws.

**Community library.** The community library is served by our Vercel-hosted backend, which retrieves library content from Supabase.

- **Searching:** search terms you type are sent to our backend as part of the request and used to query the library database.
- **Saving a community snippet:** the Extension downloads the public snippet from our server and stores it locally. Your private snippets are not sent to the backend.

Our application code does not intentionally log search terms. However, Vercel and Supabase may process request metadata (such as IP address and request URL) in their infrastructure logs, under their own policies.

**IP addresses.** Our hosting provider, Vercel, receives your IP address when the Extension contacts our backend. Our backend does not forward your IP address to Google Analytics. Our application code uses request IP addresses only for short-lived, in-memory rate limiting and does not store them in a database. Vercel and Supabase may process IP addresses in their logs.

## 4. How We Use Information

We use analytics information solely to understand how often the Extension is used, identify popular features, understand how the community library is used, and improve the Extension. Library search terms are used only to return search results.

We do not use or transfer data for advertising, personalized ads, or credit or lending decisions, and we do not sell user data. We handle user data in accordance with the Chrome Web Store User Data Policy, including its Limited Use requirements.

## 5. Third-Party Services

- **Google Analytics 4:** processes pseudonymous usage events. [Google Privacy Policy](https://policies.google.com/privacy)
- **Vercel:** hosts our backend and may process technical request data such as IP addresses. [Vercel Privacy Policy](https://vercel.com/legal/privacy-policy)
- **Supabase:** hosts the community library database and may process request and infrastructure data. [Supabase Privacy Policy](https://supabase.com/privacy)

## 6. Retention

Google Analytics retains event data for **14 months**, per the retention setting on our analytics property. Identifiers stored locally on your device remain until removed (see Section 2). Infrastructure logs at Vercel and Supabase are retained according to their own policies. We do not otherwise store your snippets or search terms.

## 7. Extension Permissions

- `storage`: stores analytics identifiers, interface settings, and local SnippetShelf data.
- `clipboardWrite`: copies snippets to your clipboard when you choose.
- `activeTab` and `scripting`: let the Extension open its panel on the page you are viewing, only when you click the toolbar icon or use the keyboard shortcut. The Extension does not read page text, selections, URLs, or titles.
- `offscreen`: creates a background document so the Extension can write to the clipboard, which the service worker cannot do.
- Host permission (`https://browser-vault-g2x041wjc-bilal-mohammed-s-projects.vercel.app/*`): communicates with our backend for analytics and the community library.

## 8. Your Choices and Privacy Rights

You can stop future analytics collection by uninstalling the SnippetShelf extension. Uninstalling also removes locally stored extension data, but does not automatically delete analytics data already processed by Google Analytics.

Depending on where you live, you may have rights over your personal information, such as the right to access it, request correction or deletion, or object to or opt out of certain processing. To make a privacy request or ask a question, email us using the contact details below. We will review and respond in accordance with applicable data protection laws. Because our analytics use pseudonymous identifiers rather than names or email addresses, we may need additional information, such as your client ID, to locate analytics records associated with your installation. We may be unable to identify or retrieve specific records if we cannot reliably associate them with your request.

## 9. Data Security

We take reasonable measures to protect information we process. The GA4 API secret is held on our backend and is not included in the distributed extension. No method of transmission or storage is completely secure.

## 10. Children's Privacy

SnippetShelf is not directed at children, and we do not knowingly collect personal information from children.

## 11. Changes to This Policy

We will post any updates at this URL and revise the effective date above.

## 12. Contact

**Developer:** Bilal Mohammed
**Email:** bilalmohammed333999@gmail.com