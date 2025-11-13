# PHP Environment for Laragon

| PHP | XDebug |
| --  | ------ |
| `PHP 7.4 VS16 (x64, TS)` | [`v3.1.6`](https://xdebug.org/download/historical#3_1_6) |
| `PHP 8.0 VS16 (x64, TS)` | [`v3.1.5`](https://xdebug.org/download/historical#3_1_5) |
| `PHP 8.1 VS16 (x64, TS)` | [`v3.3.2`](https://xdebug.org/download/historical#3_3_2) |
| `PHP 8.2 VS16 (x64, TS)` | [`v3.2.0`](https://xdebug.org/download/historical#3_2_0) |
| `PHP 8.3 VS16 (x64, TS)` | [`v3.3.2`](https://xdebug.org/download/historical#3_3_2) |
| `PHP 8.4 VS17 (x64, TS)` | [`v3.4.7`](https://xdebug.org/download/historical#3_4_7) |


### PHP Extension
- Default

  `curl`, `fileinfo`, `gd`, `intl`, (`mbstring, exif`), `mysqli`, `openssl`, `pdo_mysql`, `xsl`.

- Optional

  `gmp`, `pdo_sqlite`, `sockets`, `sodium`, `sqlite3`, [`xdebug`](https://xdebug.org/), `zip`.


### Quick Tutorial

1. Download PHP TS (because the `php8apache2_4.dll` file only exists in TS).
2. Edit file `etc\apache2\mod_php.conf`

    ```diff
    # This file is auto-generated, so please keep it intact.
    - LoadModule php_module "G:/laragon/bin/php/php-8.2.11-Win32-vs16-x64/php8apache2_4.dll"
    - PHPIniDir "G:/laragon/bin/php/php-8.2.11-Win32-vs16-x64"
    + LoadModule php_module "G:/laragon/bin/php/php-8.3.6-Win32-vs16-x64/php8apache2_4.dll"
    + PHPIniDir "G:/laragon/bin/php/php-8.3.6-Win32-vs16-x64"
    <IfModule mime_module>
        AddType application/x-httpd-php .php
    </IfModule>
    ```

    If `LoadModule php8_module`, change to `LoadModule php_module`.

3. Make sure that PHP 8.3 uses `httpd-2.4.59-win64-VS17` or higher.


### References
- https://windows.php.net/download/
- https://www.apachelounge.com/download/
- https://xdebug.org/download/historical
