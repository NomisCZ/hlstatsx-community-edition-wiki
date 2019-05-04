## 🚀 Getting Started
1. Download latest HLStatsX from repository [here](https://github.com/NomisCZ/hlstatsx-community-edition/archive/master.zip)
2. Extract **.zip** file


## 🗄 Database
1. Create new database and database user
> Before you create the database it is recommended that you enable utf8mb4 encoding (utf8mb4_unicode_ci). This is because some players may have special characters that utf8 (The default encoding for MySQL) does not support.
2. Grant the user permissions to access the new database
3. Import SQL -> **sql/install.sql**
   * phpMyAdmin - `Databases -> <db_name> -> Import -> Choose File -> Go`
   * Command line: `mysql -u<db_user> -p<db_user_password> <db_name> < install.sql`

## 🌍 Website
1. Upload **web/*** to your webhosting
2. Edit **config.php** and fill `DB_NAME, DB_USER, DB_PASS, DB_ADDR`
3. Remove **updater** directory

## ⚡️ Daemon
### ⭕️ Linux
### ✔️ 1. Prerequisites

**1.1. Install build-essential (make)** ⚠️ (Without this package you won't be able to build & install Perl packages!)

* Ubuntu/Debian:
```
$ sudo apt install build-essential
$ sudo apt install libssl-dev
$ sudo apt install zlib1g-dev
```
* CentOS:
```
$ sudo yum groupinstall 'Development Tools'
$ sudo yum install openssl-devel
$ sudo yum install zlib-devel
```

**1.2. Install Perl MySQL**

* Ubuntu/Debian:
```
$ sudo apt install libdbd-mysql-perl
```
* CentOS:
```
$ sudo yum install perl-DBD-MySQL
```

**1.3. Install OpenSSL**

* Ubuntu/Debian:
```
$ sudo apt install openssl
```
* CentOS:
```
$ sudo yum install openssl
```

**1.4. Install unzip**

* Ubuntu/Debian:
```
$ sudo apt install unzip
```
* CentOS:
```
$ sudo yum install unzip
```

**1.5. Install Perl packages**

**1.5.1. Open Perl package manager**
```
$ perl -MCPAN -e shell
$ type yes (first run only)
```

**1.5.2. Install GeoIP2::Database::Reader package**
```
cpan> install GeoIP2::Database::Reader
```

**1.5.2. Install Syntax::Keyword::Try package**
```
cpan> install Syntax::Keyword::Try
```
### ✔️ 2. Installation

**2.1. Download latest HLStatsX from repository and extract files**

```
$ wget https://github.com/NomisCZ/hlstatsx-community-edition/archive/master.zip
$ unzip master.zip
```

**2.2. Prepare enviroment**

```
$ mv hlstatsx-community-edition-master/scripts ./
$ rm -R hlstatsx-community-edition-master master.zip
$ chmod +x hlstats-awards.pl hlstats.pl hlstats-resolve.pl run_hlstats
```

**2.3. Prepare config**
* Edit **hlstats.conf** in your favourite editor (`eg. nano hlstats.conf`) and fill `DBHost, DBUsername, DBPassword, DBName`

**2.4. Prepare GeoIP2** _(optional)_

```
$ cd GeoLiteCity
$ chmod +x install_binary.sh
$ ./install_binary.sh
```

***

### ⭕️ Windows
### ✔️ 1. Prerequisites

**1.1. Install ActivePerl** ⚠️ (Without this software you won't be able to run daemon!)
* https://www.activestate.com/products/activeperl/downloads/

**1.2. Install Perl packages**

**1.2.1. Open Perl package manager**
* Open CMD as Administrator (`Start -> CMD -> Right click on it -> Run as administrator`)
```
C:\WINDOWS\system32> ppm
```

**1.2.2. Install DBI / DBD-mysql packages**
```
cpan> install DBI
cpan> install DBD-mysql
```

**1.2.3. Install GeoIP2::Database::Reader package**
```
cpan> install GeoIP2::Database::Reader
```

**1.2.4. Install Syntax::Keyword::Try package**
```
cpan> install Syntax::Keyword::Try
```

### ✔️ 2. Installation

**2.1. Download latest HLStatsX from repository and extract files**
* https://github.com/NomisCZ/hlstatsx-community-edition/archive/master.zip
* Extract **.zip** file and keep only **scripts** folder (you can delete other folders)

**2.2. Prepare config**
* Edit **hlstats.conf** in your favourite editor (`eg. Notepad++`) and fill `DBHost, DBUsername, DBPassword, DBName`

**2.4. Prepare GeoIP2** _(optional)_
* Download latest database: https://geolite.maxmind.com/download/geoip/database/GeoLite2-City.tar.gz
* Open downloaded **.tar.gz** file (`eg. in WinRAR`) and copy **GeoLite2-City.mmdb** to **scripts/GeoLiteCity**
