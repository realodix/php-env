# PHP Environment

| PHP | XDebug |
| --  | ------ |
| `PHP 7.4 VS16 (64 bit)` | `v3.1.5` |
| `PHP 8.0 VS16 (64 bit)` | `v3.1.5` |
| `PHP 8.1 VS16 (64 bit)` | `v3.1.5` |
| `PHP 8.2 VS16 (64 bit)` | `v3.2.0` |
| `PHP 8.3 VS16 (64 bit)` | `v3.3.2` |


### PHP Extension
- Default

  `curl`, `fileinfo`, `gd`, `intl`, (`mbstring, exif`), `mysqli`, `openssl`, `pdo_mysql`, `xsl`.

- Optional

  `gmp`, `pdo_sqlite`, `sockets`, `sodium`, `sqlite3`, [`xdebug`](https://xdebug.org/download), `zip`.


### Quick Tutorial

1. Download PHP TS (karena file `php8apache2_4.dll` hanya ada di TS).
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

    Jika `LoadModule php8_module`, ganti ke `LoadModule php_module`.

3. Pastikan pada PHP 8.3 menggunakan `httpd-2.4.59-win64-VS17` atau versi yang lebih tinggi.


### References
- https://windows.php.net/download/
- https://www.apachelounge.com/download/
- https://xdebug.org/download
