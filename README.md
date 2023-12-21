# Deployment crud basic local




## Travail a faire

Déployez le CRUD de base sur le serveur local

### Critére de validation

- Realiser lab crud basic apres deployement
- Utiliser server apache pour le deployment
- Migration base donne automatique

### Commande

```bash
Use illuminate\Support\Facades\Artisan

# Ajouter ce commande au AppServicesProviders sur function registre()

Artisan::call('migrate');

# Config apache mettre ce code dans le fichier httpd.conf

<IfModule ssl_module>
SSLRandomSeed startup builtin
SSLRandomSeed connect builtin
</IfModule>

<VirtualHost 192.168.1.245:80>
    ServerName app.local
    DocumentRoot "C:\Apache24\htdocs\lab-crud-basic\public\index.php"
    <Directory "C:\Apache24\htdocs\lab-crud-basic\public\index.php">
        Options FollowSymLinks
        AllowOverride All
        Require all granted
        DirectoryIndex index.php
    </Directory>
</VirtualHost>


LoadModule php_module "C:\php-8.1.25\php8apache2_4.dll"
AddType application/x-httpd-php .php
PHPIniDir "C:\php-8.1.25"

# 
```

### Solution

[crud-basic](http://192.168.1.245/)


### Reference

[Medium](https://adeyomoladev.medium.com/how-to-deploy-a-laravel-app-using-apache-and-mysql-4910a07f9a0c)
