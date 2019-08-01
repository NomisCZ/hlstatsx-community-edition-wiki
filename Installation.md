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
### 👉 Linux
### 1. Prerequisites

**1.1. Install build-essential (make)** ⚠️ (Without this package you won't be able to build & install Perl packages!)

* Ubuntu/Debian:
```console
root@vm:~$ apt install build-essential
root@vm:~$ apt install libssl-dev
root@vm:~$ apt install zlib1g-dev
```
* CentOS:
```console
root@vm:~$ yum groupinstall 'Development Tools'
root@vm:~$ yum install openssl-devel
root@vm:~$ yum install zlib-devel
```

**1.2. Install Perl MySQL**

* Ubuntu/Debian:
```console
root@vm:~$ apt install libdbd-mysql-perl
```
* CentOS:
```console
root@vm:~$ yum install perl-DBD-MySQL
```

**1.3. Install OpenSSL**

* Ubuntu/Debian:
```console
root@vm:~$ apt install openssl
```
* CentOS:
```console
root@vm:~$ yum install openssl
```

**1.4. Install unzip**

* Ubuntu/Debian:
```console
root@vm:~$ apt install unzip
```
* CentOS:
```console
root@vm:~$ yum install unzip
```

**1.5. Install Perl packages**

**1.5.1. Open Perl package manager**
```console
root@vm:~$ perl -MCPAN -e shell
cpan> type yes (first run only)
```

**1.5.2. Install MaxMind::DB::Reader package**
```console
cpan> install MaxMind::DB::Reader
```

**1.5.3. Install GeoIP2::Database::Reader package**
```console
cpan> install GeoIP2::Database::Reader
```

**1.5.4. Install Syntax::Keyword::Try package**
```console
cpan> install Syntax::Keyword::Try
```
### 2. Installation

**2.1. Download latest HLStatsX from repository and extract files**

```console
user@vm:~$ wget https://github.com/NomisCZ/hlstatsx-community-edition/archive/master.zip
user@vm:~$ unzip master.zip
```

**2.2. Prepare enviroment**

```console
user@vm:~$ mv hlstatsx-community-edition-master/scripts ./
user@vm:~$ rm -R hlstatsx-community-edition-master master.zip
user@vm:~$ cd scripts
user@vm:~$ chmod +x hlstats-awards.pl hlstats.pl hlstats-resolve.pl run_hlstats
```

**2.3. Prepare config**
* Edit **hlstats.conf** in your favourite editor (`eg. nano hlstats.conf`) and fill `DBHost, DBUsername, DBPassword, DBName`

**2.4. Prepare GeoIP2** _(optional)_

```console
user@vm:~$ cd GeoLiteCity
user@vm:~$ chmod +x install_binary.sh
user@vm:~$ ./install_binary.sh
```

***

### 👉 Windows
### 1. Prerequisites

**1.1. Install ActivePerl** ⚠️ (Without this software you won't be able to run daemon!)
* ⚠️ **Use only version <= 5.2.4. Newer version no longer included Perl Package Manager and some packages are incompatible.**

* ActiveState platform (registration needed): https://platform.activestate.com/ActiveState/ActivePerl-5.24/auto-fork
* If you don't want to register on their boring ActiveState plaform (totally useless): https://github.com/NomisCZ/hlstatsx-community-edition/raw/master/ActivePerl/ActivePerl-5.24.3.2404-MSWin32-x64-404865.exe

**1.2. Install Perl packages**

**1.2.1. Open Perl package manager**
* Open CMD as Administrator (`Start -> CMD -> Right click on it -> Run as administrator` OR use PowerShell)
```console
C:\WINDOWS\system32> ppm
```
* Switch view to "All packages"
![](https://i.imgur.com/SnNfhM8.png)

**1.2.2. Install packages**
* Type name of the package to the search bar, then right click on the package and click on Install.
![](https://i.imgur.com/4Kq8VBO.png)
* After you have selected all packages listed below click on the green arrow (or <kbd>Ctrl+Enter</kbd>)
![](https://i.imgur.com/oD78D8f.png)
* **DBI** - Database independent interface for Perl
* **DBD-mysql** - A MySQL driver for the Perl5 Database Interface (DBI)
* **Throwable** - a role for classes that can be thrown
* **MaxMind-DB-Reader** - Read MaxMind DB files and look up IP addresses
* **MaxMind-DB-Common** - Code shared by the MaxMind DB reader and writer modules
* **Data-IEEE754** - Pack and unpack big-endian IEEE754 floats and doubles
* **GeoIP2** - Perl API for MaxMind's GeoIP2 web services and databases
* **Data-Validate-IP** - IPv4 and IPv6 validation methods
* **NetAddr-IP** - Manages IPv4 and IPv6 addresses and subnets
* **Syntax-Keyword-Try** - a C<try/catch/finally> syntax for perl

### 2. Installation

**2.1. Download latest HLStatsX from repository and extract files**
* https://github.com/NomisCZ/hlstatsx-community-edition/archive/master.zip
* Extract **.zip** file and keep only **scripts** folder (you can delete other folders)

**2.2. Prepare config**
* Edit **hlstats.conf** in your favourite editor (`eg. Notepad++`) and fill `DBHost, DBUsername, DBPassword, DBName`

**2.4. Prepare GeoIP2** _(optional)_
* Download latest database [here](https://geolite.maxmind.com/download/geoip/database/GeoLite2-City.tar.gz)
* Open downloaded **.tar.gz** file (`eg. in WinRAR`) and copy **GeoLite2-City.mmdb** to **scripts/GeoLiteCity**
