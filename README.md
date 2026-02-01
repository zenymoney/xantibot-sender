# Xantibot Sender
High-performance mass email software with advanced anti-spam algorithms and multi-SMTP support for fast, reliable, and secure delivery.

## Requirements

- PHP 8.2 or higher  
- PHP extensions: cURL
- Windows or Linux OS 


## Features

### Rotation System
| Feature             | Description |
|--------------------|-------------|
| SMTP                | Automatic rotation between multiple SMTP accounts |
| Subject             | Dynamic subject line rotation for campaigns |
| From Name / Email   | Rotate sender name and email addresses |
| Proxy               | Use proxies for sending emails |
| Link                | Rotate or randomize links in email content |
| Letter                | Rotate letter |

### Generate / Tag System

| Feature                    | Description |
|---------------------------|-------------|
| Text Random Generator      | Generate random text to avoid pattern detection |
| Time                       | Insert dynamic timestamps |
| UUID                       | Generate unique identifiers per message |
| Device / OS / Browser      | Emulate different devices, operating systems, and browsers |
| IP                         | Inject dynamic IP values |
| Country Name / Code        | Insert country name or ISO country code |
| User-Agent                | Randomize User-Agent headers |
| Domain TLD                | Customize top-level domains dynamically |
| Custom Tag                | Define custom placeholders for content |
| Obfuscation (Anti-Filter)  | Obfuscate content to reduce spam filter detection |

## Email Sending Modes

| Mode        | Main File        | Account/Relay Source      | Key Feature                        | Short Description                              |
|-------------|------------------|--------------------------|-------------------------------------|------------------------------------------------|
| Gmail API   | mode-gmail.php   | google-token.list         | Send via Gmail API                | Bypass Gmail SMTP limit, more stable           |
| SMTP        | mode-smtp.php    | smtp.list                | Send via direct SMTP                | Supports any SMTP server                       |
| Proxy SMTP  | mode-proxy.php   | smtp.list + proxy.list   | SMTP via Proxy/non-proxy             | Mass SMTP, dynamic IP, anti-blocking           |

### Short Explanation
- **mode-gmail**: Sends email using Gmail API , suitable for bypassing Gmail SMTP limits and more stable delivery.
- **mode-smtp**: Sends email using direct SMTP server, can use any email account that supports SMTP.
- **mode-proxy**: Same as mode-smtp, but each SMTP connection can use a proxy (SOCKS/HTTP), suitable for mass sending to avoid IP blocking.

## File Structure

```
├── attachment/              # Email attachments
├── core/                    # Core PHP classes and utilities
├── documentation/           # Guides and documentation
├── Gauth/                   # Google Auth (Node.js scripts, tokens)
├── list/                    # All configuration lists (recipients, smtp, etc)
├── private-tools/           # Private tools and logs
├── template/                # Email HTML templates
├── vendor/                  # Composer dependencies (PHPMailer, Google API, etc)
├── xantibot-php/            # Xantibot PHP binaries/libraries
├── composer.json            # Composer dependencies config
├── config.php               # Main configuration file
├── mode-gmail.php           # Gmail API sending mode
├── mode-smtp.php            # SMTP sending mode
├── mode-proxy.php           # SMTP with proxy mode
├── run.mode-proxy.bat       # Windows batch to run proxy mode
├── run.mode-smtp.bat        # Windows batch to run SMTP mode
└── readme.md                # Project documentation
```


## Next Update Plan

| Feature / Improvement         | Description                                      | Status    |
|------------------------------|--------------------------------------------------|-----------|
| mode-gscli                   | Send Email using gmailapp using Google Scripts    | Planned   |

