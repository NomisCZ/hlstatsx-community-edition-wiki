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
### Linux
1. Prerequisites
  1.2. Test


### Windows