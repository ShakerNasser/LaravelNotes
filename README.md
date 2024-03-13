# Create a Laravel Project

To get started with Laravel, you need to follow several steps to create your project. Below is a step-by-step guide to creating a new Laravel project.

1. **Create a Laravel project**:
   First and foremost, you need to create a Laravel project if you haven't already. This can be done using Composer by running the following command in the terminal:

- composer create-project --prefer-dist laravel/laravel project-name

2. **Create a database migration**:
Run the following command in the terminal to create a database migration:

php artisan make:migration create_pages_table

* Open the created migration file in `database/migrations` and define the schema for your table. *

3. **Run migrations**:
Run the following command to run the migration and create the table in the database:

php artisan migrate

4. **Create a model**:
Create a model for the page by running the following command:

php artisan make:model Page

5. **Create a controller**:
Create a controller to handle the logic for the page:

php artisan make:controller PageController

Open the created controller file in `app/Http/Controllers` and add methods to display the page.

6. **Define routes**:
Open `routes/web.php` and define a route to display the page:
```php
use App\Http\Controllers\PageController;

Route::get('/page', [PageController::class, 'show']);

---------------------------------------------------------

Create a view:
Create a Blade view to display the page. You can create a new file page.blade.php in the resources/views directory and add the HTML code for your page.

Handle CSRF token:
To handle the CSRF token, it is automatically included in Laravel forms by using the @csrf directive inside the form. For example:

<form method="POST" action="/page">
    @csrf
    <!-- Form fields -->
</form>

-------------------------------------------------------------------------------

This guide provides an overview of the various steps required to create a Laravel project and how you can continue to build your application. Good luck with your Laravel development! 🚀
