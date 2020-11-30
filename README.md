[![Issues](https://img.shields.io/github/issues/hemantjr/package-export?style=flat-square)](https://github.com/hemantjr/package-export/issues)
[![Stars](https://img.shields.io/github/stars/hemantjr/package-export?style=flat-square)](https://github.com/hemantjr/package-export/stargazers)
## EXPORT LIBRARY for Laravel

###
### Laravel Export for export data into PDF,EXCEL & CSV.

Require this package in your composer.json and update composer. This will download the package also.

    composer require xpert/export

## Installation

### Laravel 8.x:

After updating composer, add the ExportServiceProvider to the providers array in `config/app.php`

    Xpert\Export\ExportServiceProvider::class,

You can optionally use the facade for shorter code. Add this to your facades:

    'Export' => Xpert\Export\Facade\Export::class,

## Using

You can easily use Export using `use Export` statement.

    <?php
        use Export;
        class ....{
            public function ...(){
                return Export::exportExcel($args)
            }
        }
    ?>
    
### License

This EXPORT Wrapper for Laravel is open-sourced software licensed.
 