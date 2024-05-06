# renovate-config
My personally fine-tuned [Mend Renovate](https://www.mend.io/renovate-free/) configuration

# Key Features
- Follows [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/)
- Updates only non-major versions by default (Avoids breaking changes)
- Enables Renovate commit signing
- Enables `Dependency Dashboard` for quick overview of dependencies
- & more!

## Usage
Add `"github>kiruyuto/renovate-config"` to `extends` section in your`renovate.json` file, so it looks like this:
```json
{
  "$schema": "https://docs.renovatebot.com/renovate-schema.json",
  "extends": [ "github>kiruyuto/renovate-config" ]
}
```

## How to configure it further?
You can override any of the [settings](https://docs.renovatebot.com/configuration-options/) in this configuration by adding them to your `renovate.json` file.  
For example, to change the conventional commits `scope` and use `dependencies` instead of `deps`, you can add the following to your `renovate.json` file, below the `extends` section:
```jsonc
{
  "$schema": "https://docs.renovatebot.com/renovate-schema.json",
  "extends": [ "github>kiruyuto/renovate-config" ], // Please note this has default scope of "deps"
  "semanticCommitScope": "dependencies" // This will override commit scope to "dependencies"
}
```

## Validate the configuration
You can validate the configuration in this repo by running the following command:
```bash
# Install dependencies and run validation. 
# Installation is required only once.
bun install && bun run validate
```
or check the official docs how to [validate](https://docs.renovatebot.com/config-validation/) your own file!
