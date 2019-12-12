<p align="center">
    <a href="https://github.com/yiisoft" target="_blank">
        <img src="https://avatars0.githubusercontent.com/u/993323" height="100px">
    </a>
    <h1 align="center">Yii 2 Advanced Project Quick Start Template</h1>
    <br>
</p>

An quick start package with all the pretty SEO-friendly URL enabled for both frontend and backend. The application is built using advanced pattern and has a modular structure.

REQUIREMENTS
-------------------

The minimum requirement by this project template that your Web server supports PHP 5.5.0.

INSTALLTAION
-------------------

Clone the repository

```
git clone https://github.com/depakmurthy/yii2-advanced-quickstart.git
cd yii2-advanced-quickstart
composer install
```
DATABASE
-------------------

import the `yii2_advanced_quick_start.sql` file from this repository to your `mysql server`.
Database with name `yii2_advanced_quick_start` is created.

Config file - `common\config\main-local.php` update the `components` array

```
'db' => [
    'class' => 'yii\db\Connection',
    'dsn' => 'mysql:host=localhost;dbname=yii2_advanced_quick_start',
    'username' => 'root',
    'password' => 'toor',
    'charset' => 'utf8',
],
```

SEO-FRIENDLY URL
-------------------

Frontend - Update rules, if any new URLs in `frontend\config\main.php`
```
'rules' => [
    "" => "site/index",
    "about" => "site/about",
    "contact" => "site/contact",
    "signup" => "site/signup",
    "login" => "site/login",
    "request-password-reset" => "site/request-password-reset",
    "resend-verification-email" => "site/resend-verification-email"
],
```
Backend - Update rules, if any new URLs in `backend\config\main.php`

```
'rules' => [
    "" => "site/login"
],
```

DIRECTORY STRUCTURE
-------------------

```
common
    config/              contains shared configurations
    mail/                contains view files for e-mails
    models/              contains model classes used in both backend and frontend
    tests/               contains tests for common classes    
console
    config/              contains console configurations
    controllers/         contains console controllers (commands)
    migrations/          contains database migrations
    models/              contains console-specific model classes
    runtime/             contains files generated during runtime
backend
    assets/              contains application assets such as JavaScript and CSS
    config/              contains backend configurations
    controllers/         contains Web controller classes
    models/              contains backend-specific model classes
    runtime/             contains files generated during runtime
    tests/               contains tests for backend application    
    views/               contains view files for the Web application
    web/                 contains the entry script and Web resources
frontend
    assets/              contains application assets such as JavaScript and CSS
    config/              contains frontend configurations
    controllers/         contains Web controller classes
    models/              contains frontend-specific model classes
    runtime/             contains files generated during runtime
    tests/               contains tests for frontend application
    views/               contains view files for the Web application
    web/                 contains the entry script and Web resources
    widgets/             contains frontend widgets
vendor/                  contains dependent 3rd-party packages
environments/            contains environment-based overrides
```
