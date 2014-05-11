AistThemes
==========

Zend Framework 2 module that allows developers install &amp; switch between various themes for their projects.

## Features
 * Theme Installer

## Requirements
 * Zend Framework 2.3.0 or later.
 * PHP 5.4.0 or later.

## Installation using [Composer](http://getcomposer.org)
 1. Open console (command prompt)
 2. Go to your application's directory.
 3. Run `composer require aist/aist-themes:dev-master`

Theme Installer
===============

AistThemes relies on specific directory locations for templates and plugins.
By default [Composer](http://getcomposer.org) is unable to install in an other
directory than /vendor except when using a
[Custom Installer](http://getcomposer.org/doc/articles/custom-installers.md).

This Theme Installer for Composer will trigger on the following library types
and provide custom behaviour for those.

* *aist-theme*, install files into /data/themes instead of /vendor

Creating your own themes
------------------------

In order to tell a theme to use this installer you need to add the following
*composer.json*

```
{
    "name": "aist/theme-$NAME$",
    "type": "aist-theme",
    "require": {
        "aist/aist-themes": "*"
    }
}
```

The type element will instruct Composer to use this Theme Installer.
