# Permission Drift CI Landing Page

Static validation landing page for Permission Drift CI.

Permission Drift CI is positioned as a pre-merge review tool for Chrome extension repositories. It helps maintainers identify risky permission and configuration drift before changes are merged.

## Included pages

- `index.html` — landing page with product explanation, checks, test pricing, and waitlist form.
- `thanks.html` — confirmation page for successful waitlist submissions.
- `styles.css` — static CSS for the landing page.

## Checks described

The page explains review signals for:

- `<all_urls>` permission changes
- Manifest V2 usage
- `eval` and `new Function`
- Remote scripts
- Problematic CSP changes
- Privacy drift

## Waitlist form

The waitlist form posts to FormSubmit for `permissiondriftci@gmail.com` and includes:

- Name
- Email
- Project stage
- Optional message
- Honeypot spam field
- FormSubmit standard captcha behavior
- Subject: `Novo lead — Permission Drift CI`
- Redirect to `thanks.html`

Submitted data is described as being used only to respond about the waitlist and related product validation.

## Constraints

This validation page intentionally does not include Stripe, payments, analytics, Chrome Web Store Marketplace integrations, frameworks, or external dependencies. It does not promise Chrome Web Store approval.

## Local testing

Run a local static server from the repository root:

```bash
python3 -m http.server 8000
```

Then open:

- <http://127.0.0.1:8000/index.html>
- <http://127.0.0.1:8000/thanks.html>
