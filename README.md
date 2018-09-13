# Metatags
A Laravel package to fetch all metadata of a website.

## Installation
Perform the following operations in order to use this package
- Run `composer require "mobiosolutions/metatags"` in your terminal
- **Add Service Provider** 
   Open `config/app.php` and add `mobiosolutions\metatags\Providers\MetatagsProvider::class,` to the end of `providers` array:

    ```
    'providers' => array(
        ....
        mobiosolutions\metatags\Providers\MetatagsProvider::class,
    ),
    ```
   Next under the `aliases` array:

    ```
    'aliases' => array(
        ....
        'Metatags' => mobiosolutions\metatags\Facades\MetatagsFacade::class
    ),
    ```
## Requirements
- You need to install the [DOM](http://www.php.net/en/dom) extension.

## How to use

- After following the above steps, 

    ```
    // Add to your controller
    use Metatags;

    $metadata = Metatags::get("https://example.com/");

    print_r($metadata);
    ```