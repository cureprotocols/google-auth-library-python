# google-auth-lite

[![PyPI version](https://img.shields.io/pypi/v/google-auth-lite.svg)](https://pypi.org/project/google-auth-lite/)
[![License](https://img.shields.io/pypi/l/google-auth-lite.svg)](https://github.com/cureprotocols/google-auth-rewired/blob/main/LICENSE)
[![Python](https://img.shields.io/pypi/pyversions/google-auth-lite.svg)](https://pypi.org/project/google-auth-lite/)

> A lightweight Google Auth SDK for service accounts and OAuth2 login — clean, modern, and developer-focused.

---

## 🚀 Install

```bash
pip install google-auth-lite
```

---

## 🔐 Features

- ✅ Clean service account auth with `GoogleAuthLite`
- ✅ OAuth2 login flow with `GoogleOAuthFlow`
- ✅ Minimal dependencies, fast startup
- ✅ Flask example: OAuth login in under 60 seconds
- ✅ Dev-first: no config wizards, no Google UI bloat

---

## ✨ Quickstart

### Service Account (backend auth)

```python
from google_auth_rewired import GoogleAuthLite

auth = GoogleAuthLite("path/to/your-service-account.json", scopes=["https://www.googleapis.com/auth/drive"])
session = auth.authorized_session()

r = session.get("https://www.googleapis.com/drive/v3/files")
print(r.json())
```

### OAuth2 Login (user auth)

```python
from google_auth_rewired import GoogleOAuthFlow

flow = GoogleOAuthFlow(
    client_id="your-client-id",
    client_secret="your-client-secret",
    scopes=["openid", "email", "profile"],
    redirect_uri="http://localhost:5000/callback"
)

# Step 1: Get login URL
print(flow.auth_url())

# Step 2: Handle callback URL and get token
token = flow.fetch_token("http://localhost:5000/callback?code=...")
```

---

## 📂 Examples

- `examples/oauth_web_flow.py` — Flask app with Google Login
- `examples/drive_basic.py` — List files in Drive
- `examples/sheets_read.py` — Read Google Sheets
- `examples/gmail_send.py` — Send email via Gmail API
- `examples/gcs_upload.py` — Upload file to Google Cloud Storage

---

## 🧪 Testing

```bash
pytest tests/
```

---

## 🧠 Author

Built with precision by [cureprotocols](https://github.com/cureprotocols)

---

## 🧾 License

MIT — use freely, modify confidently, deploy globally.
```

---