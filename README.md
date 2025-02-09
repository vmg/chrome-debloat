# Chrome Debloat

A tool to generate policies for Chromium-based browsers (Chrome, Brave, and Edge) that disable unnecessary features, telemetry, and bloatware while enabling some quality-of-life improvements.

## Features

- Attempts to disable telemetry and usage reporting
- Removes unnecessary features and pre-installed bloatware
- Blocks promotional content and unnecessary UI elements
- Maintains browser functionality while reducing resource usage
- Pre-configures essential extensions:
  - uBlock Origin
  - Cookie AutoDelete
  - Don't f*** with paste
  - I still don't care about cookies
  - SponsorBlock
  - BlockTube
  - BlankTab
  - Decentraleyes

### Supported Browsers

| Browser | Windows | macOS | Linux |
|---------|---------|-------|-------|
| Google Chrome | ✅ | ✅ | ❌ |
| Microsoft Edge | ✅ | ✅ | ❌ |
| Brave | ✅ | ✅ | ❌ |

## Quick Start

### Windows
1. Download the `.reg` file for your browser from the `generated/windows/` directory
2. Double click to import the registry settings
3. Restart your browser or visit `chrome://policy` and click "Reload Policy" 

### macOS
1. Download the `.mobileconfig` file for your browser from the `generated/macos/` directory
2. Double click to install the profile
3. Approve the profile installation in System Settings > Privacy & Security > Profiles
4. Restart your browser or visit `chrome://policy` and click "Reload Policy" 

## Custom Configuration

If you want to customize the policies:

1. Clone this repository
2. Install dependencies:
   ```bash
   uv sync
   ```
3. Modify `policies.yaml` according to your needs
4. Generate new configuration files:
   ```bash
   uv run main.py
   ```
5. Find the generated files in `generated/` directory

## Policy Documentation

- [Chrome Enterprise Policies](https://chromeenterprise.google/policies/)
- [Brave Policies](https://support.brave.com/hc/en-us/articles/360039248271-Group-Policy)
- [Microsoft Edge Policies](https://learn.microsoft.com/en-us/deployedge/microsoft-edge-policies)

## License

[Apache 2.0](./LICENSE)
