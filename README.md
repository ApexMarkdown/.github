# ApexMarkdown

**One Markdown processor to rule them all**

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

ApexMarkdown is the home of **Apex**, a universal Markdown processor that combines the best features from CommonMark, GitHub Flavored Markdown (GFM), MultiMarkdown, Kramdown, and more. We're building a single, unified tool that lets you use all the popular Markdown extensions and features without having to choose between incompatible processors.

## 🚀 About Apex

Apex is designed to end the fragmentation in the Markdown ecosystem. Instead of being forced to pick one Markdown flavor and give up features from others, Apex supports multiple compatibility modes and includes the most popular features from all major Markdown processors.

### Key Features

- **Multiple Compatibility Modes**: CommonMark, GFM, MultiMarkdown, Kramdown, and Unified (all features)
- **Advanced Tables**: GitHub-style tables with rowspan, colspan, captions, per-cell alignment, and more
- **Footnotes**: Three syntaxes supported (reference-style, Kramdown inline, MultiMarkdown inline)
- **Citations & Bibliography**: Pandoc, MultiMarkdown, and mmark citation styles with BibTeX/CSL support
- **Task Lists**: GitHub-style checkboxes for to-do items
- **Math Support**: LaTeX math expressions with inline and display modes
- **Wiki Links**: `[[Page Name]]` syntax with configurable formatting
- **Smart Typography**: Automatic conversion of quotes, dashes, and ellipses
- **Syntax Highlighting**: External highlighting via Pygments or Skylighting
- **Extensibility**: Plugin system for custom syntax and post-processing
- **Filter System**: AST filters for document transformations

### Output Formats

- Compact HTML fragments
- Pretty-printed HTML
- Complete standalone HTML5 documents
- Full control over styling and accessibility (ARIA support)

## 📦 Main Repositories

### [Apex](https://github.com/ApexMarkdown/apex)
The core Markdown processor written in C++ for speed and reliability. This is where all the magic happens.

**Installation:**
```bash
# Homebrew (macOS/Linux)
brew tap ttscoff/thelab
brew install ttscoff/thelab/apex

# Or download pre-built binaries from releases
```

**Basic Usage:**
```bash
apex input.md -o output.html
apex input.md --standalone --pretty --title "My Document"
```

### [Apex Filters](https://github.com/ApexMarkdown/apex-filters)
A collection of AST (Abstract Syntax Tree) filters that transform Markdown documents before rendering. Filters can be written in any language (Ruby, Python, Lua, etc.) and process the document structure programmatically.

**Available Filters:**
- **title**: Automatically adds a level-1 header from document metadata
- **delink**: Converts links to plain text
- **uppercase**: Converts all text to uppercase
- **unwrap**: Unwraps elements for custom HTML handling

**Installing Filters:**
```bash
apex --install-filter title
apex --install-filter delink
apex --filter title input.md > output.html
```

### [Apex Plugins](https://github.com/ApexMarkdown/apex-plugins)
A directory of plugins that extend Apex with new syntax patterns and post-processing capabilities. Plugins are opt-in and execute during specific processing phases.

**Using Plugins:**
```bash
apex --list-plugins
apex --install-plugin kbd
apex --plugins input.md > output.html
```

Or enable per-document with metadata:
```yaml
---
plugins: true
---
```

## 🎯 Use Cases

- **Technical Documentation**: Generate beautiful docs with tables, code highlighting, and math
- **Academic Writing**: Citations, footnotes, and bibliographies with multiple format support
- **Note-Taking**: Wiki links, task lists, and callouts for personal knowledge bases
- **Blog Posts**: Smart typography, syntax highlighting, and GitHub emoji support
- **Books & Reports**: Multi-file includes, tables of contents, and indices

## 📚 Documentation

- [Apex Wiki](https://github.com/ApexMarkdown/apex/wiki) - Complete documentation
- [Syntax Reference](https://github.com/ApexMarkdown/apex/wiki/Syntax) - All supported syntax
- [Command Line Options](https://github.com/ApexMarkdown/apex/wiki/Command-Line-Options) - CLI reference
- [Citations Guide](https://github.com/ApexMarkdown/apex/wiki/Citations) - Using citations and bibliographies
- [Plugins Guide](https://github.com/ApexMarkdown/apex/wiki/Plugins) - Creating and using plugins

## 🤝 Contributing

We welcome contributions to all ApexMarkdown repositories! Whether it's bug reports, feature requests, documentation improvements, or code contributions, your help is appreciated.

- **Core Processor**: Contribute to [apex](https://github.com/ApexMarkdown/apex)
- **Filters**: Add new filters to [apex-filters](https://github.com/ApexMarkdown/apex-filters)
- **Plugins**: Share plugins via [apex-plugins](https://github.com/ApexMarkdown/apex-plugins)

## 📄 License

All ApexMarkdown projects are licensed under the MIT License. See individual repositories for details.

## 🔗 Links

- [Apex Releases](https://github.com/ApexMarkdown/apex/releases) - Download the latest version
- [Issue Tracker](https://github.com/ApexMarkdown/apex/issues) - Report bugs or request features
- [Discussions](https://github.com/ApexMarkdown/apex/discussions) - Ask questions and share ideas