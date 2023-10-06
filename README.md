# Assessment of Stallion Express

## Task 1:

- I have created a command console for retrieving the property details from API
- Artisan Command has to be executed to make the API on daily basis. It can be changed based on the client need.

"php artisan app:daily-property-update"

To activate the scheduled jobs, run the Cron command from the Cron Jobs Manager.

"/public_html/artisan schedule:run"

## Task 2: CRUD of Property

Using VueJS, CRUD functionality for property has been done.

1. Created Model with MCR for property.
2. In Database migration, property table has been created with requirement fields.
3. In PropertyController, code for list all properties, new property, update existing property, deleting property, view property and search properties has been implemented.
4. Next, In welcome blade file, ("resources/views/welcome.blade.php"), APP container was added to import vue component into it.
5. In resources/js/app.js, App view created with necessary components for property is added.


## VUE Pages:

- Default home page view, App vue (resources/js/components/App.vue) is added to show the list of properties with actions (view, edit and delete) which default calls to Property List component (/components/PropertyList.vue). Also there is a button for creating new property. Also, a text field to search the properties based on country and description. Additional fields of search can be added.

- Property View component ("/components/PropertyView.vue") is to show details of selected property.

- Property Form component ('./components/PropertyForm.vue') consists of both add and update functionality of the property with image upload and resizing it to thumpnail.


# INSTALLATION AND CONFIGURATION:

1. Git clone the application from github.
2. In the respective directory of the application, run command

```
composer update
npm install
```
3. Create new ENV file and update the database credentials.
4. Run
```
php artisan migrate
```
to migrate the tables into the database.
5. To run console command to retrieve the property from API, run this command
```
php artisan app:daily-property-update
```
6. Finally, in first terminal run php artisan serve to run laravel application. In second terminal, run npm run dev to VUE JS.

I have created a folder "screenhost" to show you outputs of this application.

Thanks!



