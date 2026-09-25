# cdo

Salesforce DX project created with Orchard.

- `force-app/` holds the metadata. Orchard's pre- and post-deployment actions live in `force-app/scripts/` and `force-app/data/`.
- `config/project-scratch-def.json` is the standard Salesforce DX definition. Generate the project's definition from the Dev Hub in Orchard (Setup → Definition) and copy it here.
- `npm ci` installs the lint, format and test tools. `npm run lint`, `npm test` and `npm run prettier:verify` are the checks Orchard's agents run.

Create a scratch org on your machine:

```bash
sf org create scratch --definition-file config/project-scratch-def.json --alias cdo --target-dev-hub <your Dev Hub alias>
```

## CI

Pull requests to `main` run Orchard validation via `.github/workflows/pr-validate.yml` (secrets `ORCHARD_URL`, `ORCHARD_CI_TOKEN`).
