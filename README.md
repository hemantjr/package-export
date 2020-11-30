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

## Dependencies ( automatically downlaoded with package )

    - maatwebsite/excel
    - barryvdh/laravel-dompdf

## Export Excel or Csv
To Export Excel or Csv run command `php artisan make:export UserExport(name) --model=User(model name)`.
above command create file `UserExport.php` inside `App >> Exports >> userExport.php`.
You can easily use Export using `use Export` statement.

    <?php
        use Export;
        class ....{
            public function ...(){
                // $data = new UserExport.php
                return Export::exportExcel($data,'file_name');
                return Export::exportCsv($data,'file_name');
            }
        }
    ?>
    
## Export Pdf
To Export Pdf simply pass `Model::all()` inside method like below example.

    <?php
        use Export;
        class ....{
            public function ...(){
                return Export::exportPdf(User::all(),'file_name');
            }
        }
    ?>


### License

This EXPORT Wrapper for Laravel is open-sourced software licensed.
 