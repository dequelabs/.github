# .github

## Generating an Anthropic API Key

Follow these steps to generate an API key for the Anthropic (Claude) API:

1. **Go to the Anthropic Console**
   Visit [console.anthropic.com](https://console.anthropic.com) and sign in or create an account.

2. **Navigate to API Keys**
   In the left sidebar, click **API Keys**.

3. **Create a new key**
   Click **Create Key**, give it a descriptive name, then click **Create Key** to confirm.

4. **Copy and store your key**
   The key is shown **only once** — copy it immediately and store it securely (e.g., in a password manager or as a secret in your CI/CD environment).

### Using the key

Set the key as an environment variable:

```bash
export ANTHROPIC_API_KEY="sk-ant-..."
```

Or store it as a GitHub Actions secret:
- Go to your repository → **Settings** → **Secrets and variables** → **Actions**
- Click **New repository secret**, name it `ANTHROPIC_API_KEY`, and paste the key.

### Security notes

- Never commit API keys to source control.
- Rotate keys regularly and revoke any that may have been exposed.
- Use least-privilege access — create separate keys per project or environment.
