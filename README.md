Text editor
-https://download.sublimetext.com/Sublime%20Text%20Build%203176%20x64%20Setup.exe

import urllib.request,os,hashlib; h = '6f4c264a24d933ce70df5dedcf1dcaee' + 'ebe013ee18cced0ef93d5f746d80ef60'; pf = 'Package Control.sublime-package'; ipp = sublime.installed_packages_path(); urllib.request.install_opener( urllib.request.build_opener( urllib.request.ProxyHandler()) ); by = urllib.request.urlopen( 'http://packagecontrol.io/' + pf.replace(' ', '%20')).read(); dh = hashlib.sha256(by).hexdigest(); print('Error validating download (got %s instead of %s), please try manual install' % (dh, h)) if dh != h else open(os.path.join( ipp, pf), 'wb' ).write(by)


direct download
https://www.apachefriends.org/xampp-files/7.1.23/xampp-win32-7.1.23-0-VC14-installer.exe
>php -v


-----Installing Laravel-------

First
Laravel utilizes Composer to manage its dependencies. So, before using Laravel, make sure you have Composer installed on your machine.


Download the installer file by accessing the direct download link: https://getcomposer.org/Composer-Setup.exe
 or visiting the official download page: https://getcomposer.org/download
>composer -v



#install specific version
composer create-project --prefer-dist laravel/laravel=5.5.* VMP_laravel

#install new latest version
composer create-project --prefer-dist laravel/laravel VMP_laravel


laravel cli
>php artisan key:generate
it is in .env.
If the application key is not set, your user sessions and other encrypted data will not be secure!

>php artisan serve

Authentication

>php artisan make:auth

Auth::routes() is just a helper class that helps you generate all the routes required for user authentication.

migration

>php artisan make:migration create_categories_table
>php artisan make:migration create_categories_table


learn at https://laravel.com/docs/5.7/migrations#generating-migrations for datatype

>php artisan migrate:fresh

seeding
>php artisan make:seeder CategoriesTableSeeder
>php artisan db:seed

>php artisan db:seed --class=SpecificTableSeeder
>php artisan migrate:refresh --seed
>php artisan make:model Category

Contoller
>php artisan make:controller CategoryController --resource
