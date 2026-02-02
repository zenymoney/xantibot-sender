## Installation

### Ubuntu / Debian

```bash
# Update system packages
sudo apt update && sudo apt upgrade -y

# Install PHP 8 and required extensions
sudo apt install -y php8.1 php8.1-cli php8.1-curl php8.1-mbstring php8.1-xml php8.1-mysql unzip curl

# Verify PHP version and cURL extension
php -v
php -m | grep curl
```

### CentOS / RHEL / AlmaLinux

```bash
# Enable EPEL and Remi repository
sudo dnf install -y epel-release
sudo dnf install -y https://rpms.remirepo.net/enterprise/remi-release-9.rpm
sudo dnf module reset php
sudo dnf module enable php:remi-8.1 -y

# Install PHP 8 and extensions
sudo dnf install -y php php-cli php-curl php-mbstring php-xml php-mysqlnd unzip curl

# Verify installation
php -v
php -m | grep curl
```
