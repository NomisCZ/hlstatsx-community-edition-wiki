## 🗄 Database
* MySQL 5.5+ (5.7.x recommended)
> Before you create the database it is recommended that you enable utf8mb4 encoding (utf8mb4_unicode_ci). This is because some players may have special characters that utf8 (The default encoding for MySQL) does not support.
## 🌍 Website
* Apache / Nginx / IIS
* PHP 5.6+ (7.x recommended)
* PHP Extensions
  * Curl
  * MySQLi 
## ⚡️ Daemon

### 👉 Linux
* Perl 5
* Perl packages
  * GeoIP2::Database::Reader
  * Syntax::Keyword::Try
* Linux packages
  * build-essential (Development Tools)
  * libssl-dev (openssl-devel)
  * zlib1g-dev (zlib-devel)
  * libdbd-mysql-perl (perl-DBD-MySQL)
  * openssl
  * unzip

***

### 👉 Windows
* ActivePerl
* Perl packages
  * DBI
  * DBD::mysql
  * GeoIP2::Database::Reader
  * Syntax::Keyword::Try
> Other packages that are required to install are individual.