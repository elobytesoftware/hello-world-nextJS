This is a [Next.js](https://nextjs.org) project bootstrapped with [`create-next-app`](https://nextjs.org/docs/app/api-reference/cli/create-next-app).

## Getting Started

First, run the development server:

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
# or
bun dev
```

# 1) make a new keypair just for GitHub Actions (no passphrase to keep it simple)
ssh-keygen -t ed25519 -C "gh-actions" -f ~/.ssh/gh_actions -N ""

# 2) allow that public key to log in
cat ~/.ssh/gh_actions.pub >> ~/.ssh/authorized_keys
chmod 700 ~/.ssh
chmod 600 ~/.ssh/authorized_keys

# Step 2 — Put the private key into GitHub Secrets (replace old)

Still on EC2 (to copy the private key text):

cat ~/.ssh/gh_actions