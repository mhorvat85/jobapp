# jobapp

Job Application

## Technologies

Project is created with:

- PHP
- SQLite
- Tailwind CSS

## Requirements for viewing this app

- php, php dev server | apache, composer package manager, extension=pdo_sqlite & extension=sqlite3 (php.ini)

## Recommendations for SQLite extension

- SQLite3 Editor

## Run(dev server)

- php -S localhost:8000 -t public

## Setup and Run(apache)

- in **httpd.conf** file

  - LoadModule rewrite_module modules/mod_rewrite.so
  - DirectoryIndex index.php index.html
  - Include conf/extra/httpd-vhosts.conf

- in **httpd-vhosts.conf** file

```
<VirtualHost *:80>
    ServerName jobapp
    DocumentRoot "${SRVROOT}/htdocs/jobapp/public"
    <Directory "${SRVROOT}/htdocs/jobapp/public">
        Options Indexes FollowSymLinks
        AllowOverride All
        Require all granted
    </Directory>
</VirtualHost>
```

- in **hosts** file (e.g. C:\Windows\System32\drivers\etc\hosts)

```
127.0.0.1   jobapp
```

- in web browser

```
localhost
```
