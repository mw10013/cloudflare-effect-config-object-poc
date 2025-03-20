# cloudflare-effect-config-object-poc

Proof-of-Concept (POC) for `object` support in Effect's Config. See [Ask](./Ask.md) for motivation and details.

- https://cloudflare-effect-config-object-poc-production.devxo.workers.dev/

## Local Dev

- pnpm i
- pnpm dev

## Deploy

- pnpm wrangler kv namespace create cloudflare-effect-config-object-poc-kv-production
- Update wrangler.jsonc production kv_namespaces
- CLOUDFLARE_ENV=production pnpm build
- pnpm wrangler deploy
- Workers & Pages Settings: cloudflare-effect-config-object-poc
  - Git repository: connect to git repo
  - Build configuration
    - Build command: CLOUDFLARE_ENV=production build
    - Deploy command: pnpm wrangler deploy


