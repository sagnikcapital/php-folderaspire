# Content
> Automating folder generation in PHP can be done using the mkdir() function, which is used to create directories. Here's a brief example of how you can automatically generate folders:
- Custom PHP
- Wordpress

## Dependencies
- PHP (8.0)
- Apache 2

## Installation
>Please follow this steps, and also refer the code blocks for ths setup using php dependency  manager (composer).
Open terminal and run this command.
```sh
$ composer install
```

```sh
$ composer require sagnikrivud/php-folderaspire
```
```sh
$ composer dump-autoload
```
Use the Service Provider class at PHP file after auto  loading configuration:

```php
require __DIR__ . '/vendor/autoload.php';
```
```php
use  Sagnikd\FolderAspire\Folder;
```
```php
$manageFolder = new Folder();
```
> create a folder with permission
```php
$manageFolder->createDirectory('path/to/directory_name', 775);
```
> Import directory from an existing parent directory
```php
$manageFolder->importDirectory('source/dir','destination/dir');
```

> Get proper location or Path of a Folder or File
```php
$manageFolder->getFolderLocation('folderName/fileName');
```

> Get a Namespace of Class or Service provider
```php
$manageFolder->recoverNamespace('folderName','path/to/folder');
```
> Lock a directory
```php
$manageFolder->lockDirectory('folder', 'path/to/folder');
```

> Base/root directory
```php
'Base' => env('BASE_ROOT', __DIR__),
```
