# Kaspa Websites

A decentralized web platform built on the Kaspa blockchain. Create, encrypt, and navigate HTML websites stored permanently on-chain.

![Version](https://img.shields.io/badge/version-2.0.0-blue)
![License](https://img.shields.io/badge/license-MIT-green)
![Kaspa](https://img.shields.io/badge/blockchain-Kaspa-purple)

## 🌟 Features

### Core Features
- 📝 **Create HTML Websites** - Store websites permanently on the Kaspa blockchain
- 🔒 **Encryption** - Password-protect your websites with AES-256-GCM encryption
- 🔗 **Decentralized Navigation** - Link between blockchain pages using transaction IDs
- 🖼️ **Image Support** - Embed images as base64 or use external HTTPS images
- 🌐 **Chrome Extension** - Easy viewing of blockchain websites
- 💾 **Permanent Storage** - Immutable, censorship-resistant content

### Advanced Features
- Password visibility toggle
- Double-encoding detection and handling
- Comprehensive HTML detection
- Content Security Policy injection for external resources
- Transaction ID link interception
- Encrypted payload detection

## 🚀 Quick Start

### Web Interface

1. Open `web/kaspa-websites-complete.html` in a browser
2. Connect your KasWare wallet
3. Create or view blockchain websites

### Chrome Extension

1. Extract `extension/` folder
2. Add icon files (16x16, 48x48, 128x128 PNG)
3. Load in Chrome:
   - Go to `chrome://extensions/`
   - Enable "Developer mode"
   - Click "Load unpacked"
   - Select the extension folder

## 📁 Project Structure

```
kaspa-websites/
├── web/
│   └── kaspa-websites-complete.html    # Main web application
├── extension/
│   ├── manifest.json                   # Extension manifest
│   ├── popup.html                      # Extension popup UI
│   ├── popup.js                        # Extension logic
│   └── README.md                       # Extension documentation
├── docs/
│   ├── IMPLEMENTATION_GUIDE.md         # Implementation details
│   ├── FEATURES.md                     # Feature documentation
│   └── API.md                          # API reference
├── examples/
│   └── sample-websites/                # Example websites
├── LICENSE
└── README.md                           # This file
```

## 🛠️ How It Works

### Creating a Website

1. **Write HTML** - Create your HTML content
2. **Optional Encryption** - Toggle encryption and set a password
3. **Embed Images** - Upload images to convert to base64
4. **Send Transaction** - Store on Kaspa blockchain via KasWare wallet
5. **Get TX ID** - Receive permanent transaction ID

### Viewing a Website

1. **Enter TX ID** - Paste the 64-character transaction ID
2. **Decrypt** (if needed) - Enter password for encrypted sites
3. **Render** - View the website in a new tab

### Linking Websites

Use transaction IDs as links:
```html
<a href="e7ea30217fa296dfce8dbcd4d2510b88535627bec9df9887919d71cef52f12bd">Next Page</a>
```

## 🔐 Encryption

Websites can be encrypted using AES-256-GCM:
- **Algorithm**: AES-256-GCM
- **Key Derivation**: PBKDF2 (100,000 iterations, SHA-256)
- **Salt**: 16 bytes (random)
- **IV**: 12 bytes (random)
- **Format**: `ENC1` marker + encrypted data

## 📊 Technical Details

### Supported Features
- ✅ HTML5 tags
- ✅ CSS (inline and external HTTPS)
- ✅ JavaScript (inline and external HTTPS)
- ✅ Images (base64 embedded or HTTPS)
- ✅ Links to other blockchain pages
- ✅ Encryption with password protection

### Limitations
- Maximum transaction size: ~100KB (compress images!)
- HTTPS images only (mixed content blocked)
- No HTTP external resources
- Base64 images increase payload size by ~33%

## 🎯 Use Cases

- **Decentralized Blogs** - Censorship-resistant content
- **Private Documents** - Encrypted, permanent storage
- **NFT Websites** - On-chain HTML for NFTs
- **Permanent Records** - Immutable documentation
- **Decentralized Wiki** - Linked knowledge base
- **Web3 Portfolios** - Permanent personal sites

## 🔧 Requirements

### For Creating Websites
- Modern web browser (Chrome, Firefox, Edge)
- [KasWare Wallet](https://www.kaswallet.io/) extension
- Kaspa (KAS) for transaction fees (~0.1 KAS per site)

### For Viewing Websites
- Chrome browser (for extension)
- OR any modern browser (for web interface)

## 📖 Documentation

- [Implementation Guide](docs/IMPLEMENTATION_GUIDE.md) - Technical implementation details
- [Features](docs/FEATURES.md) - Complete feature list
- [API Reference](docs/API.md) - Developer API documentation
- [Extension Guide](extension/README.md) - Chrome extension setup

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

### Development Setup

1. Clone the repository
2. Make your changes
3. Test thoroughly
4. Submit a PR

### Areas for Contribution
- Additional features
- Bug fixes
- Documentation improvements
- UI/UX enhancements
- Security audits

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- [Kaspa](https://kaspa.org/) - The blockchain platform
- [KasWare](https://www.kaswallet.io/) - Wallet integration
- The Kaspa community

## 📞 Support

For questions, issues, or feature requests:
- Open an [Issue](https://github.com/EthanBorg/kaspa-websites/issues)
- Visit [Kaspa Discord](https://discord.gg/kaspa)
- Check [Kaspa.org](https://kaspa.org)

## 🗺️ Roadmap

- [ ] Multi-page website templates
- [ ] Markdown support
- [ ] IPFS integration for large files
- [ ] Search functionality
- [ ] Website directory/index
- [ ] Advanced styling templates
- [ ] Video embed support (external hosting)
- [ ] RSS feed generation

## ⚠️ Disclaimer

This is experimental software. Store important data with caution. Always keep backups of encryption passwords - lost passwords cannot be recovered.

---

**Built with ❤️ for the decentralized web**

[Website](https://kaspa.org) • [Twitter](https://twitter.com/KaspaCurrency) • [Discord](https://discord.gg/kaspa)
