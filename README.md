# Laravel Email Database Log

A simple database logger for all outgoing emails sent by Laravel website. Thanks to Shvets Group for this wonderful extension 

# Requirements

- PHP 8.2+
- Laravel 12

# Installation

## Step 1: Composer

Laravel Email Database Log can be installed via [composer](http://getcomposer.org) by running this line in terminal:

```bash
composer require vikramsra/laravel-email-database-log
```

## Step 2: Configuration

The service provider is registered automatically via package discovery. If you have disabled package discovery, add the following to the providers list in `bootstrap/providers.php`:

```php
return [
    // ...
    vikramsra\LaravelEmailDatabaseLog\LaravelEmailDatabaseLogServiceProvider::class,
];
```

## Step 3: Migration

Publish migration files:
```bash
php artisan vendor:publish --tag=laravel-email-database-log-migration
```

Now, run this in terminal:
```bash
php artisan migrate
```

# Usage

After installation, any email sent by your website will be logged to `email_log` table in the site's database.
