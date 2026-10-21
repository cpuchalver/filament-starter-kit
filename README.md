# Filament Starter Kit

A Laravel starter kit with two Filament panels:

- **App panel**, served at `/`, with login and email verification
- **Admin panel**, served at `/admin`, restricted to users with the `is_admin` flag, with user management (list, create, edit, delete)

It ships with Pest, Laravel Boost and Spatie's coding guidelines for AI-assisted development.

## Requirements

- PHP 8.3+
- Composer
- Node.js and npm
- The [Laravel installer](https://laravel.com/docs/installation#installing-php)

## Installation

Create a new project with the Laravel installer:

```bash
laravel new my-project --using=https://github.com/cpuchalver/filament-starter-kit
```

The installer downloads the starter kit without its Git history, installs the dependencies, generates the application key, creates and migrates the database, and builds the frontend assets.

To skip the prompts and create a private GitHub repository for the new project:

```bash
laravel new my-project --using=https://github.com/cpuchalver/filament-starter-kit \
    --database=sqlite --npm --github="--private"
```

Creating the GitHub repository requires the [`gh` CLI](https://cli.github.com), authenticated with `gh auth login`.

### Create the admin user

The installer does not seed the database. Create the default admin user with:

```bash
cd my-project
php artisan db:seed
```

You can then log in with `test@example.com` / `password`. Change these credentials before deploying.

### Alternative: GitHub template

You can also click **Use this template** on GitHub, clone the new repository, and run:

```bash
composer run setup
php artisan db:seed
```

## Development

Start the development server:

```bash
composer run dev
```

Run the tests:

```bash
php artisan test --compact
```

## License

This starter kit is open-sourced software licensed under the [MIT license](https://opensource.org/licenses/MIT).
