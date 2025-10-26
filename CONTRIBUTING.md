# Contributing to VPN Kill Switch

First off, thank you for considering contributing to VPN Kill Switch! 🎉

## How Can I Contribute?

### 🐛 Reporting Bugs

Before creating bug reports, please check the existing issues to avoid duplicates.

**When reporting a bug, please include:**
- macOS version
- Python version
- VPN client you're using
- Detailed steps to reproduce
- Expected vs. actual behavior
- Log output (if available)

**Example:**
```
**macOS Version:** 14.0 Sonoma
**Python:** 3.11
**VPN:** NordVPN
**Issue:** Kill Switch doesn't detect VPN connection

**Steps to Reproduce:**
1. Connect to NordVPN
2. Activate Kill Switch
3. Icon stays red

**Logs:**
[12:34:56] VPN check: No utun interface found
```

### 💡 Suggesting Features

We love feature suggestions! Please create an issue with:
- Clear description of the feature
- Use case / why it's needed
- Possible implementation ideas

### 🔧 Pull Requests

1. **Fork the repository**
2. **Create a feature branch**
   ```bash
   git checkout -b feature/amazing-feature
   ```
3. **Make your changes**
4. **Test thoroughly**
   ```bash
   sudo python3 vpn_killswitch_final.py
   ```
5. **Commit with clear messages**
   ```bash
   git commit -m "Add amazing feature"
   ```
6. **Push to your fork**
   ```bash
   git push origin feature/amazing-feature
   ```
7. **Open a Pull Request**

### 📝 Code Style

- **Python 3.7+** compatible
- **PEP 8** compliant
- **Type hints** where appropriate
- **Comments** for complex logic
- **Docstrings** for functions/classes

**Example:**
```python
def check_vpn_connection(self) -> bool:
    """
    Checks if VPN is currently active.
    
    Returns:
        bool: True if VPN connected, False otherwise
    """
    # Implementation here
    pass
```

### 🧪 Testing

Before submitting, please test:
- ✅ Fresh installation
- ✅ VPN detection with your VPN client
- ✅ Kill Switch activation/deactivation
- ✅ Log viewer functionality
- ✅ Restart function
- ✅ Uninstall process
- ✅ macOS compatibility

### 📚 Documentation

If you change functionality, please update:
- README.md
- FINAL_ANLEITUNG.md
- Code comments
- Docstrings

## Development Setup

```bash
# Clone your fork
git clone https://github.com/yourusername/vpn-killswitch.git
cd vpn-killswitch

# Install dependencies
pip3 install rumps requests --break-system-packages

# Run in development mode
sudo python3 vpn_killswitch_final.py

# View logs
tail -f /var/log/vpn-killswitch.log
```

## Code Structure

```
vpn_killswitch_final.py
├── OptimizedFirewall      # Firewall management
├── OptimizedVPNMonitor    # VPN detection
├── KillSwitchCore         # Core logic
├── MainApp                # Menu bar app
├── LogWindow              # Log viewer
├── DetailWindow           # Detail view
└── Installer              # Installation
```

## Performance Guidelines

When contributing, keep performance in mind:
- **CPU:** Keep under 0.5%
- **RAM:** Keep under 60 MB
- **Caching:** Use caching for expensive operations
- **Timeouts:** Set reasonable timeouts (3-5s)
- **Threading:** Use daemon threads for background tasks

## Security Guidelines

This is a security-focused app. Please ensure:
- **No data collection** - Privacy is paramount
- **No external connections** - Except VPN detection
- **Fail-safe** - Internet stays blocked on error
- **Minimal privileges** - Only request what's needed
- **Clear warnings** - Users must understand actions

## Questions?

Feel free to:
- Open an issue for questions
- Email: blenkers85@icloud.com
- Start a discussion on GitHub

## Recognition

Contributors will be:
- Listed in README.md
- Mentioned in release notes
- Credited in About dialog (for major contributions)

Thank you for helping make VPN Kill Switch better! 🙏
