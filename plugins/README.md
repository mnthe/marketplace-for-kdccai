# Plugins Directory

This directory contains all Claude Code plugins available in this marketplace.

## Structure

Each plugin should be organized in its own directory with the following structure:

```
plugin-name/
├── SKILL.md              # Main plugin documentation
├── agents/               # Optional: Custom agents
├── commands/             # Optional: Custom commands
├── hooks/                # Optional: Hooks for automation
└── [other files]         # Any other plugin-specific files
```

## Adding Your Plugin

1. Create a new directory with your plugin name
2. Add a SKILL.md file with comprehensive documentation
3. Include any necessary scripts, configurations, or resources
4. Update the marketplace.json file to list your plugin
5. Test your plugin before submitting

## Plugin Template

See [PLUGIN_TEMPLATE.md](./PLUGIN_TEMPLATE.md) for a template to get started.
