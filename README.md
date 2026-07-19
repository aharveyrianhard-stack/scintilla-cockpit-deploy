# scintilla-cockpit-deploy

Deploy pipeline for **scintillahub.ai** (Vercel project `scintilla-cockpit`).

- Everything under `hub_deploy/` is the site. Push a change there → GitHub Action deploys to production.
- SAFETY GUARD: deploys are skipped until `hub_deploy/.sync_ok` exists (added only after the full site content is synced fresh).
- Required repo secret: `VERCEL_TOKEN`.
