# sovryn-dapp


## Deployment
- all PR's will be deployed as previews to tesnet network with random url
- merged PR's to branches will deploy as:
  - to `development` branch as `test.sovryn.app` with testnet env.
  - to `staging` branch as `staging.sovryn.app` with production env.
  - to `main` branch as production build with random url for additional QA, after it's tested for the last time admin can publish release to be pinned on `live.sovryn.app`.
  - to any other branch - staging deployment will be triggered with random url.
- more rules about deployment can be added to `netlify.toml` config file.

