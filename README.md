# sovryn-dapp


## Deployment
- all PR's will be deployed as previews to tesnet network with random url
- merged PR's to branches will deploy as:
  - to `development` branch as `test.sovryn.app` with testnet env.
  - to `staging` branch as `staging.sovryn.app` with production env.
  - to `main` branch as production build with random url for additional QA, after it's tested for the last time admin can publish release to be pinned on `live.sovryn.app`.
  - to any other branch - staging deployment will be triggered with random url.
- more rules about deployment can be added to `netlify.toml` config file.

### Skip deploy
Sometimes, you may want to push commits to your branch without triggering a deploy on Netlify. To do this, add [skip ci] or [skip netlify] anywhere in the Git commit message.

In the case of multiple commits pushed together, add [skip ci] or [skip netlify] to the most recent commit, and it will apply to all other commits in the push.

The next commit pushed without one of those messages will trigger a new deploy, including all changes from the skipped commits as well. To trigger a deploy at will on your production branch, go to your site’s Deploys page and select Trigger deploy at the top of the deploy list.

