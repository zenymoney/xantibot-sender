# Changelog

All notable changes to this project will be documented in this file.

---

## [Unreleased]
- Planned: mode-gscli (Send Email using GmailApp via Google Scripts)
- Planned: BCC support for all modes (mode-gmail, mode-smtp, mode-proxy)

---

## [3.0.0] - 2026-02-01
### Added
- Initial public release
- Email sending modes:
  - **Gmail API**: Send email using Gmail API (OAuth), bypass Gmail SMTP limits, more stable delivery
  - **SMTP**: Send email using direct SMTP server, supports any SMTP account
  - **SMTP with Proxy**: Each SMTP connection can use a proxy (SOCKS/HTTP), suitable for mass sending to avoid IP blocking
- Batch sending with configurable limits and delays
- Custom header support
- Attachment and embedded image support (inline attachments)
- Proxy support for SMTP
- Dot trick for Gmail sender randomization
- Reply-To customization
- Multi-account rotation (SMTP/Google tokens, sender, subject, etc)
- Error handling & informative logging
- PHPMailer integration with advanced features
- Multi-threaded sending

### Fixed
- Tag `##link##` works in all modes (mode-gmail, mode-proxy, mode-smtp)
- Google-token rotation in mode-gmail
- CID images in all modes using tag `{cid:namefile.jpg}`
- Letter rotation / multi-letter support in all modes

---

## [Features Overview]
- **Rotation**: Letter, SMTP/Auth, Subject, From Name/Email, Proxy, Link.
- **Tag Generation**: Time, Random Text, UUID, Device, and more.
- **Email Sending Modes**: Gmail API, SMTP, SMTP with Proxy.
- **Mail Sending**: TO and BCC support.
- **OS Support**: Linux and Windows.
- **Proxy Support**: Full support for SMTP connections via SOCKS/HTTP proxy (mode-proxy).
- **CID Images**: Load and embed images in email body with random Content-ID and filename.
- **Obfuscation Letter**: Obfuscate email content for better deliverability and anti-spam.
- **Xantibot Private Module**: Advanced features and tools for SMTP-proxy mode.
- **Google Auth Integration**: Helper scripts and token management in google-auth/.
- **Core Libraries**: Modular PHP classes for extensibility (core/).
- **Batch Files**: Easy Windows execution via .bat files.
- **Template System**: HTML email templates in template/.
- **Flexible Configuration**: All settings and lists managed via text files in list/.
- **Attachment & Embedded Images**: Attach files and embed images easily.
- **Multi-threaded Sending**: High throughput with parallel sending.
