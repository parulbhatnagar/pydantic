## pydantic — repository notes

This repository contains experiments and notebooks for working with LLMs and LangChain-like tooling.

WARNING: Do NOT commit real secrets into this repository. Use environment variables locally or a secret manager.

Setup
1. Copy the example env and fill in your secrets locally (do not commit):

```bash
cp .env.example .env
# then edit .env and add your real keys
```

2. Activate your virtualenv (if using `.venv`):

```bash
source .venv/bin/activate
```

3. Install dependencies:

```bash
pip install -r requirements.txt
```

Rotating leaked keys
- If any keys were committed accidentally, rotate/regenerate them immediately in the provider console (OpenAI, Groq, etc.).

Keeping secrets out of git
- Add secrets to `.env` (which is ignored).
- Keep a `.env.example` with placeholder values in the repo.
- Consider using a secrets manager (Vault, AWS Secrets Manager, GitHub Secrets) for deployment.

If you need help regenerating keys or verifying no other secrets exist, I can run a quick scan for likely API-key patterns.