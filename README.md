# marketplace-for-kdccai

Claude marketplace for KDC Club activity - A collection of Claude Code plugins and skills.

## Overview

This repository serves as a Claude Code plugin marketplace, hosting single or multiple Claude plugins within the same owner. Claude Code plugins extend the capabilities of Claude with custom agents, commands, hooks, and integrations.

## Installation

### Step 1: Add the Marketplace

Add this marketplace to your Claude Code instance:

```bash
/plugin marketplace add https://github.com/mnthe/marketplace-for-kdccai
```

Or using the shorthand format:

```bash
/plugin marketplace add mnthe/marketplace-for-kdccai
```

### Step 2: Install Plugins

After adding the marketplace, you can install individual plugins from it:

```bash
/plugin install kdccai
```

You can also browse and install plugins interactively:

```bash
/plugin
```

This will open the plugin menu where you can see all available plugins from this marketplace and install them with a click.

### Verify Installation

To verify the marketplace and plugins are installed:

```bash
/plugin marketplace list    # List all marketplaces
/plugin list                # List all installed plugins
```

## Available Plugins

### kdccai Plugin

**AI-assisted coding skills for non-developers** - Build Python automation tools with guided workflows for project initialization, planning, implementation, and debugging.

**Features:**
- `/project-init` - Initialize new automation project
- `/plan` - Create implementation plans
- `/implement` - Implement tasks with TDD
- `/debug` - Systematic error debugging

**Repository:** [mnthe/kdccai-plugin](https://github.com/mnthe/kdccai-plugin)

For detailed documentation, see the [kdccai plugin README](https://github.com/mnthe/kdccai-plugin/blob/main/README.md).

## Repository Structure

```
kdccai/
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

## Adding a New Plugin

To add a new plugin to this marketplace, you have two options:

### Option 1: Reference an External GitHub Repository (Recommended)

Add a reference to an existing GitHub plugin repository in `marketplace.json`:

```json
{
  "plugins": [
    {
      "name": "your-plugin-name",
      "source": {
        "source": "github",
        "repo": "username/plugin-repo"
      },
      "description": "Brief description of what your plugin does"
    }
  ]
}
```

This approach allows the plugin to be maintained in its own repository while being discoverable through this marketplace.

### Option 2: Host Plugin Locally in this Repository

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

## Support

For issues, questions, or suggestions:
- Open an issue in this repository
- Contact: KDC Club

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Reference

For more information about Claude Code plugin marketplaces, see:
- [Claude Code Plugin Marketplaces Documentation](https://docs.claude.com/en/docs/claude-code/plugin-marketplaces)
- [Anthropic Plugin Documentation](https://www.anthropic.com/news/claude-code-plugins)
