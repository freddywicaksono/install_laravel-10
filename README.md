# Install Laravel 10

## 1. Requirement
1. PHP 8.2
2. Composer 2.x
3. XAMPP

## 2. Open Terminal with Administrator privileges
![image](https://github.com/freddywicaksono/install_laravel-10/assets/59552422/1f27952d-9f88-4fa6-9cd1-b57f8017836d)

1. set directory to xampp/htdocs
2. give command :
```
composer create-project laravel/laravel akademik
```
This will install the last version of laravel into folder: akademik

## 3. Test the Installastion
```
http://localhost/akademik/public/
```
![image](https://github.com/freddywicaksono/install_laravel-10/assets/59552422/1c71e8cf-0000-4f70-9e00-c160fd1dd5f5)

## 4. Remove public from URL
1. Move all files in public folder to root directory project
2. Edit index.php
change this script:
```php
require __DIR__.'/../vendor/autoload.php';
$app = require_once __DIR__.'/../bootstrap/app.php';
```
to:
```php
require __DIR__.'/vendor/autoload.php';
$app = require_once __DIR__.'/bootstrap/app.php';
```
3. Test the page
```
http://localhost/akademik
```
![image](https://github.com/freddywicaksono/install_laravel-10/assets/59552422/eb0157a5-0ca6-4f80-af6f-7da9550697ef)

## Protect all files under root project
1. Edit file .htaccess on root directory project
2. add this line of code:
```
<Files .env>
    Order allow,deny
    Deny from all
</Files>
```
![image](https://github.com/freddywicaksono/install_laravel-10/assets/59552422/69a65987-ffa1-4c74-92f0-1f8a533d9254)

3. Test the page
   
![image](https://github.com/freddywicaksono/install_laravel-10/assets/59552422/2420c234-64a2-4ae9-9d40-8b4b855e2a98)


