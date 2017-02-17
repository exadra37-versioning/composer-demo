# Composer Demo

The intention of this package is only to show how to use [Semantic Versioning](https://gitlab.com/exadra37-versioning/semantic-versioning) in PHP projects using [composer](https://getcomposer.org).

The last created **TAG** will be presented in the route of this project as a markdown file.

The initial **TAG** will be `1.0.0.0` represented by file `1.0.0.0.md`.

So each time a **TAG** is created `1.0.0.0.md` will be renamed to match it.

## How To Use

Lets see some examples to cover the 4 stages of [Semantic Versioning](https://gitlab.com/exadra37-versioning/semantic-versioning) schema.


### To Require Initial TAG 1.0.0.0

#### Create this `composer.json` file:

```json
{
    "repositories": [
        {
            "type": "vcs",
            "url": "https://gitlab.com/exadra37-versioning/composer-demo"
        }
    ],
    "require": {
        "exadra37-versioning/composer-demo": "1.0.0.*"
    }
}
```

#### Lets use composer to install it:

```bash
$ composer install
Loading composer repositories with package information
Updating dependencies (including require-dev)
Package operations: 1 install, 0 updates, 0 removals
  - Installing exadra37-versioning/composer-demo (1.0.0.0) Downloading: 100%
Writing lock file
Generating autoload files
```


### To Require TAG 1.0.0.1 that represents a Bug Fix

#### Now just run:

```bash
composer update
```


### To Require TAG 1.0.1.0 that represents a Code Improvement

Edit your `composer.json` and change `"exadra37-versioning/semantic-versioning": "1.0.0.*"` to `"exadra37-versioning/semantic-versioning": "1.0.*"`.

#### Now just run:

```bash
composer update
```


### To Require TAG 1.1.0.0 that represents a Backwards Incompatible change

Edit your `composer.json` and change `"exadra37-versioning/semantic-versioning": "1.0.*"` to `"exadra37-versioning/semantic-versioning": "1.*"`.

#### Now just run:

```bash
composer update
```


### To Require TAG 2.0.0.0 that represents a major Public Api change

Edit your `composer.json` and change `"exadra37-versioning/semantic-versioning": "1.*"` to `"exadra37-versioning/semantic-versioning": "2.*"`.

#### Now just run:

```bash
composer update
```
