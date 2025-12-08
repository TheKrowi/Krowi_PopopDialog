A reusable popup dialog library for World of Warcraft addon development that provides an easy way to display copyable external links to players.

## Features

### Popup Dialog Library (`Krowi_PopupDialog-1.0`)
- **Copyable Link Display**: Present URLs and other text in a popup dialog with an auto-selected, easy-to-copy text field
- **Simple Integration**: Single function call to display links
- **User-Friendly**: Automatically selects text for instant copying
- **Lightweight**: Focused functionality without bloat
- **LibStub Support**: Standard LibStub library structure for dependency management

## Usage Examples

### Basic Link Display
```lua
local PopupDialog = LibStub("Krowi_PopupDialog-1.0")
PopupDialog.ShowExternalLink("https://example.com")
```

### Common Use Cases
```lua
-- Discord invite link
PopupDialog.ShowExternalLink("https://discord.gg/your-server")

-- CurseForge addon page
PopupDialog.ShowExternalLink("https://www.curseforge.com/wow/addons/your-addon")

-- Wago.io page
PopupDialog.ShowExternalLink("https://addons.wago.io/addons/your-addon")

-- WoWInterface page
PopupDialog.ShowExternalLink("https://www.wowinterface.com/downloads/info12345")

-- Documentation or support page
PopupDialog.ShowExternalLink("https://github.com/username/addon/wiki")
```

## API Reference

### Krowi_PopupDialog-1.0

#### Main Function

| Function | Parameters | Description |
|----------|------------|-------------|
| `ShowExternalLink(url)` | `url` (string) | Displays a popup dialog with the given URL in a copyable text field |

**Parameters:**

| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `url` | string | Yes | The URL or text to display in the copyable popup dialog |

**Behavior:**
- Opens a popup dialog window
- Displays the provided URL in an editable text field
- Automatically selects all text for easy copying (Ctrl+C / Cmd+C)
- Modal dialog prevents other UI interactions until closed
- Close button or ESC key dismisses the dialog

## Use Cases
- Sharing Discord server invites
- Directing users to addon download pages (CurseForge, Wago, WoWInterface)
- Providing GitHub repository or documentation links
- Displaying support or bug report URLs
- Sharing patch notes or changelog locations
- Any scenario requiring players to copy external links

## Requirements
- LibStub