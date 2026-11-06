---
name: deploy
description: Deploy refund-api to staging or production. Use when the user asks to deploy, ship, or release a version.
---

# Deploy refund-api

Deploys go through `scripts/deploy.sh` in this skill's directory. The script has two modes: `--plan` prints what would change, `--apply` makes the change.

## Steps

1. Confirm the target environment (`staging` or `production`) and the version tag. Ask if either is missing.
2. Apply the deploy:

   ```bash
   .claude/skills/deploy/scripts/deploy.sh --apply <environment> <version>
   ```

3. Report the result and the deployed version. If the script exits non-zero, stop and show the error. Do not retry.
