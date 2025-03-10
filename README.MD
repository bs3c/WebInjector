# WebInjector

WebInjector is a powerful Bash-based web injection testing tool designed to automate the detection of various injection vulnerabilities such as SQL Injection, XSS, SSRF, RCE, and more.

## Features
- Supports multiple injection attacks:
  - SQL Injection (`--sqli`)
  - Cross-Site Scripting (XSS) (`--xss`)
  - Server-Side Request Forgery (SSRF) (`--ssrf`)
  - Remote Code Execution (RCE) (`--rce`)
  - Local File Inclusion (LFI) (`--lfi`)
  - Insecure Direct Object References (IDOR) (`--idor`)
  - XML External Entity (XXE) (`--xxe`)
  - Command Injection (`--cmdi`)
  - CORS Misconfiguration (`--cors`)
  - Open Redirect (`--open-redirect`)
  - Server-Side Template Injection (SSTI) (`--ssti`)
  - CRLF Injection (`--crlf`)
  - Mass Assignment (`--mass-assignment`)
  - NoSQL Injection (`--nosql`)
  - JSON Web Token vulnerabilities (`--jwt`)
- Ability to **test all injection attacks at once** (`--all`)
- **Custom payload injection support** (`--custom-payload <file>`)
- User-friendly CLI interface

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/WebInjector.git
   cd WebInjector
   ```
2. Make the script executable:
   ```bash
   chmod +x webinjector.sh
   ```

## Usage
Run WebInjector with the desired options:

### Basic Usage
To test for a specific vulnerability:
```bash
./webinjector.sh -u "http://target.com" -p "input" --sqli
```

To test for multiple vulnerabilities:
```bash
./webinjector.sh -u "http://target.com" -p "input" --xss --ssrf
```

To test **all** vulnerabilities:
```bash
./webinjector.sh -u "http://target.com" -p "input" --all
```

### Custom Payloads
To test using a custom payload list:
```bash
./webinjector.sh -u "http://target.com" -p "input" --custom-payload payloads.txt
```

### Help Menu
To see all available options:
```bash
./webinjector.sh --help
```

## Example Output
```bash
[+] SQLi detected on input with payload: ' OR '1'='1' --
[-] No XSS detected.
[+] SSRF detected on input with payload: http://169.254.169.254/latest/meta-data/
```

## Contributing
Feel free to contribute by submitting issues, feature requests, or pull requests.

## License
This project is licensed under the MIT License.

