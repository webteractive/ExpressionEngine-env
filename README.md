# [ExpressionEngine CMS](https://github.com/ExpressionEngine/ExpressionEngine) with [PHP dotenv](https://github.com/vlucas/phpdotenv)

An [ExpressionEngine](https://github.com/ExpressionEngine/ExpressionEngine) boilerplate that supports [PHP dotenv](https://github.com/vlucas/phpdotenv) to improve configuration management under git deployment like [Laravel Forge](https://forge.laravel.com/). [Laravel Mix](https://laravel-mix.com/) is also added to handle asset compilation with complimentary [plugin](https://github.com/webteractive/mix) to handle asset versioning URL. [Tailwind CSS](https://tailwindcss.com/docs/what-is-tailwind/) is also added because awesome and why not.

## Requirements
1. [Composer]()
2. PHP 7 or newer
3. MySQL 5.6 or newer

## Installation
1. Download this repository as zip<!-- or run `composer create-project webteractive\ExpressionEngine-env your-app`-->
2. Run `composer install` to install dependency
3. Import the `migration.sql`
4. Rename `.env.stub` to `env` and update the required keys.
5. Visit the Admin page to verify installation by going to `/admin.php`. The initial account is `admin` / `secret2019`. Make sure to update the password!

## What's inside?
A quick look at the top-level files and directories you'll see in a *ExpressionEngine-env* project.

```
.
├── assets
├── node_modules
├── public
├── system
├── vendor
├── .env.stub
├── .gitignore
├── AUTHORS.md
├── composer.json
├── composer.lock
├── LICENSE.txt
├── Makefile
├── migration.sql
├── package-lock.json
├── package.json
├── README.md
├── tailwind.js
└── webpack.mix.js
```

## The Migration SQL
The `migration.sql` is an SQL dump file of a freshly installed [ExpressionEngine](https://github.com/ExpressionEngine/ExpressionEngine) with pre-installed [mix plugin](https://github.com/webteractive/mix).

## Environment Variables
All config keys that has been assigned to the `env` helper method will not be changed via Admin. This is the key to not mess up your git on modifying configurations.

**`BASE_PATH`** - the path where your ExpressionEngine files is located. This should be the directory where the `system` directory is located. This key is **required**.

**`BASE_URL`** - the base URL. This key is **required**.

**`DB_NAME`** - the database name. This key is **required**.

**`DB_USER`** - the database user name. This key is **required**.

**`DB_PASSWORD`** - the database user password. This key is **required**.

**`ENV`** - the current environment of your ExpressionEngine install. The value should be `local` for local development to enable LiveReload. Defaults to `production`. 

**`ERROR_VISIBILITY`** - determines who can see PHP/MySQL errors when they occur. Defaults to `1`. [See](https://docs.expressionengine.com/latest/general/system-configuration-overrides.html#debug) for more details on this config key.