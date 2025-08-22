# Vault Map Generator Plugin for Obsidian

## Overview

The **Vault Map Generator** plugin automatically creates and maintains a comprehensive sitemap of your entire Obsidian vault. Similar to how CMS systems generate sitemap.xml files, this plugin creates a structured note that serves as a centralized directory of all files in your vault, organized by folders or as a flat list.

The plugin continuously monitors your vault and updates the map automatically when you add, modify, rename, or delete files, ensuring your vault map is always current and complete.

## Key Features

### 🗂️ **Complete Vault Overview**
- **Full File Inventory**: Automatically catalogs all files in your vault
- **Folder Organization**: Groups files by their parent folders with hierarchical structure
- **File Type Icons**: Visual indicators for different file types (📝 for markdown, 🖼️ for images, 📄 for PDFs, etc.)
- **File Statistics**: Display total file counts and per-folder statistics

### 🔄 **Smart Auto-Update System**
- **Real-Time Monitoring**: Automatically detects file system changes
- **Configurable Intervals**: Set custom auto-update intervals (1-60 minutes)
- **Event-Driven Updates**: Responds to file creation, modification, deletion, and renaming
- **Manual Control**: Generate or update maps on-demand using command palette

### 📁 **Flexible Organization Options**
- **Folder Grouping**: Organize files by their containing folders
- **Flat List View**: Display all files in a single alphabetical list
- **Root Folder Handling**: Special section for files in the vault root
- **Path Display**: Show relative file paths for better navigation

### 🎛️ **Advanced File Management**
- **File Type Filtering**: Include or exclude specific file types (images, PDFs, etc.)
- **Folder Exclusion**: Skip system folders like `.obsidian` and `.trash`
- **Smart File Detection**: Supports all file types with appropriate icons
- **Self-Exclusion**: Prevents the map file from including itself

### ⚙️ **Customizable Display**
- **Multiple Sorting Options**: Sort by name, creation date, or modification date
- **Metadata Display**: Optionally show file modification dates
- **File Count Statistics**: Display number of files per folder
- **Custom Map Names**: Choose any name for your vault map file

## Installation

### Manual Installation
1. Download the latest release from the [Releases](https://github.com/elenalomova/vault-map-generator/releases) page
2. Extract the files to your vault's `.obsidian/plugins/vault-map-generator/` directory
3. Restart Obsidian
4. Enable the plugin in Settings → Community Plugins

### Development Setup
1. Clone the repository into your vault's plugins folder:
   ```bash
   cd /path/to/your/vault/.obsidian/plugins
   git clone https://github.com/yourusername/vault-map-generator.git
   ```
2. Navigate to the plugin directory and install dependencies:
   ```bash
   cd vault-map-generator
   npm install
   ```
3. Build the plugin:
   ```bash
   npm run build
   ```
4. Restart Obsidian and enable the plugin

## Usage

### Getting Started
1. **Create Your First Map**: Use the command palette (`Ctrl/Cmd + P`) and search for "Create Vault Map"
2. **Automatic Updates**: The plugin will automatically update your map as you modify files
3. **Manual Updates**: Use "Update Vault Map" command for immediate updates

### Commands
- **Create Vault Map**: Generate a new vault map
- **Update Vault Map**: Manually update the existing map

### Example Output
```markdown
# Vault Map

*Automatically generated: 22.08.2025, 15:30:00*

**Total files:** 127

## 📁 Root Folder

*Files: 5*

- 📝 [[Welcome]]
- 📝 [[Daily Notes Template]]
- 📄 [[Project Guidelines]] *(Project Guidelines.pdf)*

## 📁 Projects/Web Development

*Files: 8*

- 📝 [[Website Redesign]] - *modified: 22.08.2025*
- 📝 [[Client Requirements]]
- 🖼️ [[Mockup Design]] *(mockup-v2.png)*
- ⚙️ [[Config Settings]] *(config.json)*

## 📁 Research/Academic Papers

*Files: 15*

- 📝 [[Machine Learning Overview]]
- 📄 [[Research Paper Draft]] *(draft-v3.pdf)*
- 📊 [[Data Analysis]] *(analysis.xlsx)*
```

## Configuration

### Basic Settings
- **Map File Name**: Customize the name of your vault map file (default: "Vault Map")
- **Auto Update**: Enable/disable automatic updates
- **Update Interval**: Set how frequently the map updates (1-60 minutes)

### Organization Options
- **Group by Folder**: Organize files by containing folders vs. flat list
- **Show File Count**: Display number of files in each folder
- **Show Last Modified**: Include modification dates for each file
- **Sort By**: Choose sorting method (name, creation date, modification date)

### File Type Management
- **Include Images**: Include image files (PNG, JPG, GIF, SVG, WebP)
- **Include PDFs**: Include PDF documents in the map
- **File Type Icons**: Automatic icon assignment based on file extensions

### Content Filtering
- **Exclude Folders**: Specify folders to ignore (comma-separated list)
- Default exclusions: `.obsidian`, `.trash`
- **Custom Exclusions**: Add your own folders to skip (templates, archives, etc.)

## File Type Support

The plugin recognizes and categorizes various file types with appropriate icons:

| File Type | Icon | Extensions |
|-----------|------|------------|
| Markdown Notes | 📝 | `.md` |
| Images | 🖼️ | `.png`, `.jpg`, `.jpeg`, `.gif`, `.svg`, `.webp` |
| Documents | 📄 | `.pdf`, `.txt`, `.docx` |
| Spreadsheets | 📊 | `.xlsx`, `.csv` |
| Presentations | 📊 | `.pptx` |
| Audio | 🎵 | `.mp3`, `.wav`, `.m4a` |
| Video | 🎬 | `.mp4`, `.mov`, `.avi` |
| Archives | 🗜️ | `.zip`, `.rar`, `.7z` |
| Code | ⚙️ | `.js`, `.ts`, `.py`, `.css` |
| Web | 🌐 | `.html`, `.xml` |

## Use Cases

### 📚 **Vault Organization**
- Get a bird's-eye view of your entire knowledge base
- Identify orphaned files and organizational gaps
- Track vault growth and content distribution

### 🔍 **Content Discovery**
- Find forgotten or buried files across deep folder structures
- Discover content patterns and clustering
- Navigate large vaults more efficiently

### 📊 **Vault Analytics**
- Monitor file creation and modification patterns
- Analyze content distribution across folders
- Track project progress through file organization

### 🧹 **Vault Maintenance**
- Identify duplicate or redundant files
- Clean up unused media and attachments
- Maintain consistent file organization

### 📱 **Mobile Navigation**
- Quick access to vault structure on mobile devices
- Browse files without extensive folder navigation
- Bookmark important files through the map

## Advanced Features

### 🎯 **Smart Filtering**
- **Regex Support**: Advanced pattern matching for file exclusion
- **Dynamic Exclusions**: Exclude files based on naming conventions
- **Content-Aware Filtering**: Skip empty files or specific content types

### 🔗 **Integration Features**
- **Wikilink Generation**: Automatic creation of proper Obsidian links
- **Path References**: Include file paths for disambiguation
- **Cross-Reference Support**: Compatible with other navigation plugins

### ⚡ **Performance Optimization**
- **Incremental Updates**: Only process changed files
- **Efficient Scanning**: Optimized for large vaults (1000+ files)
- **Memory Management**: Minimal resource usage during updates

## Compatibility

- **Obsidian Version**: Requires Obsidian 0.15.0 or higher
- **Platform**: Works on Desktop, Mobile, and Web versions
- **Vault Size**: Tested with vaults up to 10,000+ files
- **Themes**: Compatible with all themes and custom CSS
- **Other Plugins**: Designed to work alongside other community plugins

## Troubleshooting

### Common Issues
- **Map Not Updating**: Check if auto-update is enabled in settings
- **Missing Files**: Verify folder exclusion settings
- **Performance Issues**: Consider increasing update intervals for large vaults
- **Broken Links**: Ensure file names don't contain special characters

### Performance Tips
- Exclude large media folders if not needed
- Increase update intervals for vaults with frequent changes
- Use folder exclusions to skip temporary or cache directories

## Support & Feedback

If you encounter any issues or have suggestions for improvements:

- **Bug Reports**: [GitHub Issues](https://github.com/elenalomova/vault-map-generator/issues)
- **Feature Requests**: [GitHub Discussions](https://github.com/elenalomova/vault-map-generator/discussions)
- **Documentation**: [Wiki](https://github.com/yourusername/elenalomova/wiki)

## Contributing

Contributions are welcome! Please feel free to submit pull requests, report bugs, or suggest new features.

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Add tests if applicable
5. Submit a pull request

## Contact

If you have any issue or you have any suggestion, please feel free to reach me via i@elenalomova.online or telegram: <a href="@t.me/ElenaLomova1987">@ElenaLomova1987</a>

## Support

If you are enjoying the plugin then you can support my work and enthusiasm by at <a href="https://boosty.to/elenalomova">Boosty</a>
