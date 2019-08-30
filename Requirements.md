## 🗄 Database
* MySQL 5.5+ (5.7.x recommended)
> Before you create the database it is recommended that you enable utf8mb4 encoding (utf8mb4_unicode_ci). This is because some players may have special characters that utf8 (The default encoding for MySQL) does not support.
## 🌍 Website
* Apache / Nginx / IIS
* PHP 7.x (7.2 recommended)
* PHP Extensions
  * Curl
  * MySQLi
  * XML
  * GD
## ⚡️ Daemon

### 👉 Linux
* Perl 5
* Perl packages
  * MaxMind::DB::Reader
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
* ActivePerl - ⚠️ Use only version <= 5.24.x. Newer version no longer included Perl Package Manager and some packages are incompatible.
* Perl packages
* **DBI** - Database independent interface for Perl
* **DBD-mysql** - A MySQL driver for the Perl5 Database Interface (DBI)
* **Throwable** - a role for classes that can be thrown
* **MaxMind-DB-Reader** - Read MaxMind DB files and look up IP addresses
* **MaxMind-DB-Common** - Code shared by the MaxMind DB reader and writer modules
* **Data-IEEE754** - Pack and unpack big-endian IEEE754 floats and doubles
* **GeoIP2** - Perl API for MaxMind's GeoIP2 web services and databases
* **Data-Validate-IP** - IPv4 and IPv6 validation methods
* **NetAddr-IP** - Manages IPv4 and IPv6 addresses and subnets
* **Moo** - Minimalist Object Orientation (with Moose compatibility)
* **MooX** - Using Moo and MooX:: packages the most lazy way
* **MooX-StrictConstructor** - Make your Moo-based object constructors blow up on unknown attributes.
* **List-AllUtils** - Combines List::Util, List::SomeUtils and List::UtilsBy in one bite-sized package
* **Syntax-Keyword-Try** - a C<try/catch/finally> syntax for perl
* **Encode** - character encodings in Perl

 Other packages that are required to install are individual.