<div align="center">
  <h1>@Kiruyuto renovate-config</h1>
  <p>
    <small>My personally fine-tuned <a href="https://www.mend.io/renovate-free/">Mend Renovate</a> configuration</small>
  </p>
  <img alt="Latest Release" src="https://img.shields.io/github/v/release/kiruyuto/renovate-config"/>
</div>

# 🚀 Key Features
- Follows [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/)
- Automatically creates PR for non-major updates
- Groups all non-major updates by default in a single PR
- Major updates require manual approval in the dependency dashboard before PR is created
- Enables Renovate commit signing
- Enables `Dependency Dashboard` for quick overview of dependencies
- Assigns created PRs to the code owners
- Rebases PRs whenever conflicts arise
- Attempts to create PRs whenever your renovate config becomes out-of-date
- & more!

## 📥 Usage
Add `"github>kiruyuto/renovate-config"` to `extends` array in your`renovate.json` file, so it looks like this:
```json
{
  "$schema": "https://docs.renovatebot.com/renovate-schema.json",
  "extends": [ "github>kiruyuto/renovate-config" ]
}
```

### How to configure it further?
You can override any of the [settings](https://docs.renovatebot.com/configuration-options/) in this configuration by adding them to your `renovate.json` file.  
For example, to change the conventional commits `scope` and use `dependencies` instead of `deps`, you can add the following to your `renovate.json` file, below the `extends` section:
```jsonc
{
  "$schema": "https://docs.renovatebot.com/renovate-schema.json",
  "extends": [ "github>kiruyuto/renovate-config" ], // Please note this has default scope of "deps"
  "semanticCommitScope": "dependencies" // This will override commit scope to "dependencies"
}
```

## ✅ Validate the configuration
You can validate the configuration in this repo by running the following command:
```bash
# Install dependencies and run validation. 
# Installation is required only once.
bun install && bun run validate
```
or check the official docs on how to [validate](https://docs.renovatebot.com/config-validation/) your own file!

## 🔗 Useful Links
- [Renovate Docs](https://docs.renovatebot.com/)
- [Configuration Options](https://docs.renovatebot.com/configuration-options/)
