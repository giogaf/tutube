## Laravel PHP Framework

####Tutorial 1

######En composer.json: <br>
"require": {

    "infyomlabs/laravel-generator": "5.1.x-dev",
    "laravelcollective/html": "5.1.*",
    "infyomlabs/adminlte-templates": "5.1.x-dev"
}

######Ejecutar: composer update

######Agregar en config/app.php

Collective\Html\HtmlServiceProvider::class,
Laracasts\Flash\FlashServiceProvider::class,
Prettus\Repository\Providers\RepositoryServiceProvider::class,
\InfyOm\Generator\InfyOmGeneratorServiceProvider::class,
\InfyOm\AdminLTETemplates\AdminLTETemplatesServiceProvider::class,

######allí también los Alias:

'Form'      => Collective\Html\FormFacade::class,
'Html'      => Collective\Html\HtmlFacade::class,
'Flash'     => Laracasts\Flash\Flash::class,
 
 ######Copiar los assets  de Infyom:
 php artisan vendor:publish
 
 ######Generamos vistas autenticación y autotorización:
 
 php artisan infyom:publish 
 php artisan infyom.publish:layout
 
 #####Opcional, Agregamos en /etc/hosts
 192.168.10.10 tutube.dev
 
 ###### y en homestead.yaml
    sites
     - map: tutube.dev
       to: /midirectorio/tutube/public
    databases:   
        - tutube       
 
 
 