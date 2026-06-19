# Railwise Agent Pack

Install Railwise business agents, skills, commands, tools, templates, and themes into supported coding agents.

This repository is the standalone Agent Pack mirror for RAILWISE-CLI `v1.2.34`.

For normal RAILWISE-CLI users, install the CLI:

```bash
npm install -g railwise-ai
```

The CLI package already includes this Agent Pack and installs the default business profile automatically.

Use this standalone repository when you want to install the pack into another coding tool or a custom directory:

```bash
npx github:railwise-cn/railwise-agent-pack install --target railwise --force
npx github:railwise-cn/railwise-agent-pack install --target codex --force
npx github:railwise-cn/railwise-agent-pack install --target claude --force
npx github:railwise-cn/railwise-agent-pack install --target opencode --force
npx github:railwise-cn/railwise-agent-pack install --dest ./.railwise --force
```

Business assets are installed by default. Maintainers can install development helpers explicitly:

```bash
npx github:railwise-cn/railwise-agent-pack install --target railwise --profile dev --force
npx github:railwise-cn/railwise-agent-pack list --profile business
npx github:railwise-cn/railwise-agent-pack list --profile dev
npx github:railwise-cn/railwise-agent-pack list --profile all
```

## Release Tarball

The same pack is also published as a GitHub Release asset from RAILWISE-CLI:

```bash
tar -xzf railwise-agent-pack-<version>.tgz
cd package
# business profile is the default
node bin/install.js install --target railwise --force
node bin/install.js install --target codex
node bin/install.js list --profile business

# maintainers can install development helpers explicitly
node bin/install.js install --target railwise --profile dev --force
node bin/install.js list
```
