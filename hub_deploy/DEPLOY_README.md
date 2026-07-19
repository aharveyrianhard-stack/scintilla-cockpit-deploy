# hub_deploy — source for scintillahub.ai (Vercel project: scintilla-cockpit)

- Any push touching hub_deploy/** auto-deploys to production via .github/workflows/deploy-hub.yml
- GUARD: deploy is skipped until hub_deploy/.sync_ok exists. Add it ONLY after index.html + icons + sw.js + manifest.json here match the current live hub (fresh sync from Mac: /Users/alanharvey/SCINTILLA 0.5/_VERCEL_DEPLOY/).
- Needed repo secret: VERCEL_TOKEN (same token as Mac _secrets/VERCEL_TOKEN.txt)
- Mac-side deployer (currently live): launchd watcher on _queue/deploy_request.txt — see Research_Logs/SECTOR_ROTATION_LOG.json
- ONE source of truth rule: once .sync_ok is in place, edit hub files IN THIS REPO, not on the Mac, or re-sync before pushing.
