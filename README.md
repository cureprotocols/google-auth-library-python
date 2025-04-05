# google-auth-rewired

![Build](https://img.shields.io/badge/build-passing-brightgreen)
![License](https://img.shields.io/github/license/cureprotocols/google-auth-rewired)
![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)

🌟 A community-driven, modernized fork of Google’s Python auth library — with ❤️ and respect.

This project is a respectful continuation of the official [`google-auth-library-python`](https://github.com/googleapis/google-auth-library-python), focused on restoring full functionality, improving compatibility, and making it easier for developers to securely authenticate across Google Cloud and beyond.

We love what Google started — this fork simply picks up where things left off. No criticism. Just code.

---

## 🔧 Why this fork?

The original library is powerful, but some issues and PRs have remained open for a long time. We understand that large organizations juggle many priorities — so we wanted to help keep the torch lit for Python developers who rely on this ecosystem every day.

**`google-auth-rewired` exists to:**

- ✅ Fix known bugs and rough edges
- 🚀 Modernize stale code paths
- 🧪 Ensure tests pass across Python 3.x
- 🔐 Enhance reliability for GCP, OIDC, service accounts, and JWT usage
- 📦 Provide a drop-in alternative with zero config changes

---

## ✅ Phase 1: Complete

### 🎯 Goal

Implement a fully testable `IdentityPoolCredentials` mock class to support secure, pluggable token handling for external identity providers.

### 🧪 Tests

The mock is verified by `tests/test_identity_pool.py`, which covers:

- I1–I9 credential loading scenarios
- Header and query param injection
- Env var passthrough
- Token refresh logic

✅ All 20 tests are **passing**  
✅ CI pipeline is active  
✅ Fully isolated from broken upstream test files

---

## ▶️ How to Run Tests

1. Create virtual environment:

```bash
python -m venv env
.\env\Scripts\activate  # On Windows
```

2. Install dev requirements:

```bash
pip install -r requirements.txt
```

3. Run the core test suite:

```bash
pytest
```

> Or use the Windows helper script:
>
```bash
.\run_tests.ps1
```

---

## 📦 Installation

```bash
pip install google-auth-rewired
```

> Want to use it as a drop-in replacement?  
> You can alias it in your virtualenv or patch imports in your code. *(Docs coming soon!)*

---

## 🤝 Contributing

We’re a community of builders, not critics.  
**PRs are welcome**, **issues are open**, and **your ideas matter**.

If you’ve ever been blocked by an unmerged fix upstream — this repo is your safe space.  
Let’s move Python forward, together.

---

## 🙏 Credits

- Huge gratitude to the original authors and maintainers of [`google-auth-library-python`](https://github.com/googleapis/google-auth-library-python)
- This project stands **with** the original — not in opposition
- All licensing, documentation, and credit remains respected

---

## 🔗 Resources

- [Original Google Auth Library](https://github.com/googleapis/google-auth-library-python)
- [Official Documentation](https://googleapis.dev/python/google-auth/latest/)
- [OAuth 2.0 for Google](https://developers.google.com/identity/protocols/oauth2)

---

## 🛡️ License

**Apache 2.0** — just like the original.

---

> Let’s keep Python auth secure, simple, and moving forward 🚀
```
