# 🔓 Advanced XSS Security Testing Tool

A comprehensive, client-side Cross-Site Scripting (XSS) vulnerability scanner designed for security professionals and ethical hackers.

![Version](https://img.shields.io/badge/version-2.0.0-red)
![License](https://img.shields.io/badge/license-MIT-blue)
![Security](https://img.shields.io/badge/security-tool-red)

## ⚡ Features

### 🎯 Core Scanning Capabilities
- **Reflected XSS Testing** - Test for immediate script execution in response
- **DOM-based XSS Testing** - Detect client-side script injection vulnerabilities
- **Stored XSS Testing** - Identify persistent cross-site scripting risks
- **Blind XSS Support** - Configure callback URLs for delayed payload execution
- **Parameter Fuzzing** - Automatically discover and test additional parameters

### 📚 Extensive Payload Library
- **Basic Payloads** - Standard script injections and event handlers
- **Advanced Techniques** - SVG, iframe, and object-based payloads
- **Obfuscated Payloads** - Encoding and string concatenation bypasses
- **DOM-specific Payloads** - Client-side execution vectors
- **Polyglot Payloads** - Multi-context injection strings
- **WAF Bypass Techniques** - Advanced evasion methods

### 🛠️ Advanced Features
- **Custom Payload Management** - Save and organize your own payloads
- **Scan History** - Track and reload previous scans
- **Real-time Dashboard** - Monitor scan progress with live statistics
- **Export Results** - Download findings in JSON or CSV format
- **Custom Headers** - Configure request headers for specific environments
- **Multiple HTTP Methods** - Support for GET, POST, PUT, DELETE

## 🚀 Quick Start

### Prerequisites
- Modern web browser with JavaScript enabled
- Local web server (for proper functionality)

### Installation
1. Download the `index.html` file
2. Serve it through a local web server:
   ```bash
   # Using Python
   python -m http.server 8000
   
   # Using Node.js
   npx http-server
   
   # Using PHP
   php -S localhost:8000
   ```

3. Open your browser and navigate to `http://localhost:8000`

### Basic Usage
1. **Enter Target URL**: Specify the endpoint to test
2. **Configure Parameters**: Define which parameters to test (comma-separated)
3. **Select Scan Type**:
   - 🚀 **Quick Scan**: Basic payloads for fast assessment
   - 🔍 **Deep Scan**: Comprehensive testing with all payload types
   - ⚙️ **Custom Scan**: User-configured payload selection
   - 🔄 **Fuzz Parameters**: Discover and test hidden parameters

4. **Review Results**: Analyze vulnerabilities in the results panel

## 📋 Configuration Options

### Target Configuration
- **URL**: The endpoint to test for XSS vulnerabilities
- **Parameters**: GET/POST parameters to inject payloads into
- **HTTP Method**: Request method (GET, POST, PUT, DELETE)
- **Custom Headers**: Additional HTTP headers as JSON

### Scanning Options
- ✅ Reflected XSS Testing
- ✅ Stored XSS Testing  
- ✅ DOM-based XSS Testing
- ✅ Blind XSS Testing
- ✅ Auto-encode Payloads
- ✅ Parameter Fuzzing

### Payload Management
- Add custom payloads to the library
- Organize payloads by category and severity
- Save frequently used payloads for quick access

## 🎯 Payload Categories

### Basic
- Script tag injections
- Event handlers (onmouseover, onload, etc.)
- Basic alert and prompt executions

### Advanced
- SVG-based payloads
- Iframe and object injections
- Image error handlers

### Obfuscated
- Character encoding bypasses
- String concatenation techniques
- Unicode and hex encoding

### DOM-based
- Fragment identifier payloads
- JavaScript protocol executions
- Location-based injections

### Polyglot
- Multi-context injection strings
- HTML/JavaScript hybrid payloads
- Context-switching techniques

### WAF Bypass
- Unicode normalization bypasses
- Script tag splitting
- Alternative syntax methods

## 📊 Results Interpretation

### Vulnerability Levels
- 🔴 **Critical**: Direct script execution confirmed
- 🟡 **Suspicious**: Potential vulnerability detected
- 🟢 **Secure**: No vulnerabilities found

### Result Details
- **Parameter**: The vulnerable input parameter
- **Payload**: The successful injection vector
- **Type**: Vulnerability classification
- **Evidence**: Proof of successful execution

## 🔧 Advanced Usage

### Custom Payload Development
```javascript
// Example custom payload structure
{
  category: "Advanced",
  payload: "<svg onload=alert(document.domain)>",
  description: "SVG-based XSS vector"
}
```

### Headers Configuration
```json
{
  "User-Agent": "Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36",
  "Accept": "text/html,application/xhtml+xml,application/xml",
  "X-Custom-Header": "test-value"
}
```

### Export Formats
- **JSON**: Structured data for programmatic analysis
- **CSV**: Spreadsheet-friendly format for reporting
- **Report**: Comprehensive vulnerability assessment document

## ⚠️ Important Notes

### Legal and Ethical Use
- 🔒 **Only test systems you own or have explicit permission to test**
- 🔒 **This tool is for educational and authorized security assessment purposes only**
- 🔒 **Unauthorized testing may be illegal in your jurisdiction**

### Technical Limitations
- Client-side tool with same-origin policy restrictions
- Requires CORS headers for cross-domain testing
- Limited to browser-based detection methods
- Does not replace comprehensive security testing

### Best Practices
1. **Always test in controlled environments first**
2. **Use dedicated test systems, not production**
3. **Document findings for proper remediation**
4. **Follow responsible disclosure practices**

## 🛡️ Security Considerations

- The tool itself doesn't execute malicious payloads against unintended targets
- All testing occurs within the browser context
- No data is transmitted to external servers
- Local storage only saves your configuration and history

## 🔮 Future Enhancements

- [ ] Server-side component for expanded testing capabilities
- [ ] Integration with popular security tools
- [ ] Advanced evasion technique updates
- [ ] Collaborative payload database
- [ ] Automated reporting templates

## 📝 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🤝 Contributing

We welcome contributions from the security community:
- New payload techniques
- UI/UX improvements
- Bug fixes and optimizations
- Documentation enhancements

## 🆘 Support

For issues and questions:
1. Check the browser console for error messages
2. Ensure you're using a modern browser
3. Verify local server configuration
4. Review same-origin policy requirements

---

