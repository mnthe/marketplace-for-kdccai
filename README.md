# marketplace-for-kdccai

Claude marketplace for KDC Club activity - A collection of Claude Code plugins and skills.

## Overview

This repository serves as a Claude Code plugin marketplace, hosting single or multiple Claude plugins within the same owner. Claude Code plugins extend the capabilities of Claude with custom agents, commands, hooks, and integrations.

## Repository Structure

```
marketplace-for-kdccai/
│
├── .claude-plugin/
│   └── marketplace.json     # Marketplace manifest file
│
├── plugins/                 # Directory for all plugins
│   └── [plugin-name]/       # Individual plugin directories
│       ├── SKILL.md         # Plugin documentation
│       └── ...              # Plugin-specific files
│
└── README.md               # This file
```

## Installation

To add this marketplace to your Claude Code instance:

```bash
/plugin marketplace add https://github.com/mnthe/marketplace-for-kdccai
```

## Available Plugins

Currently, this marketplace is being initialized. Plugins will be added soon.

To browse available plugins, check the [plugins/](./plugins/) directory or view the [marketplace.json](./.claude-plugin/marketplace.json) file.

## Adding a New Plugin

To add a new plugin to this marketplace:

1. **Create a plugin directory** under `plugins/`:
   ```bash
   mkdir -p plugins/your-plugin-name
   ```

2. **Add plugin files** including:
   - `SKILL.md` - Plugin documentation and instructions
   - Any additional files, scripts, or configurations

3. **Update marketplace.json** to include your plugin:
   ```json
   {
     "plugins": [
       {
         "name": "your-plugin-name",
         "description": "Brief description of what your plugin does",
         "version": "1.0.0",
         "skills": [
           "./plugins/your-plugin-name"
         ]
       }
     ]
   }
   ```

4. **Document your plugin** with clear instructions in the SKILL.md file

## Plugin Structure Guidelines

Each plugin should contain:

- **SKILL.md**: Main documentation file describing:
  - Purpose and capabilities
  - Usage instructions
  - Examples
  - Configuration options
  
- **Additional files**: Scripts, configurations, or resources needed by the plugin

## Contributing

Contributions are welcome! To contribute:

1. Fork this repository
2. Create a new branch for your plugin or improvement
3. Add your plugin following the guidelines above
4. Submit a pull request with a clear description

## Usage

After adding this marketplace, you can install individual plugins:

```bash
/plugin install [plugin-name]
```

## Support

For issues, questions, or suggestions:
- Open an issue in this repository
- Contact: KDC Club

## License

This marketplace and its plugins are provided as-is for KDC Club activities.

## Reference

For more information about Claude Code plugin marketplaces, see:
- [Claude Code Plugin Marketplaces Documentation](https://docs.claude.com/en/docs/claude-code/plugin-marketplaces)
- [Anthropic Plugin Documentation](https://www.anthropic.com/news/claude-code-plugins)
