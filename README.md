# CODEIGNITER 3.1.11 - FIRST SETUP

## HTACCESS SETUP
1. buat file `.htaccess` pada direktori `nama_project`
2. salin kode berikut :

```
RewriteEngine On
RewriteCond %{REQUEST_FILENAME} !-f
RewriteCond %{REQUEST_FILENAME} !-d
RewriteRule ^(.*)$ index.php/$1 [L]
```


## CONFIG SETUP
1. masuk pada direktori `nama_project/application`

    ### AUTOLOAD SETUP
    1. open file `autoload.php`
    ```
    $autoload['libraries'] = array("database","session","form_validation");


    $autoload['helper'] = array("url","form","file");


    $autoload['model'] = array("model_santri");
    ```

