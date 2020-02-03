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

    ### AUTOLOAD.PHP SETUP

    1. open file `autoload.php`
    2. tambahkan value pada beberapa variabel di bawah ini

    ```
    $autoload['libraries'] = array("database","session","form_validation");


    $autoload['helper'] = array("url","form","file");


    $autoload['model'] = array("nama_ model");
    ```

    ### CONFIG.PHP SETUP

    1. open file `config.php`
    2. tambahkan value pada beberapa variabel di bawah ini

    ```
    $config['base_url'] = 'http://localhost:8888/nama_project/';

    ```
    ### DATABASE.PHP SETUP

    1. open file `database.php`
    2. tambahkan value pada beberapa variabel di bawah ini

    ```
    $db['default'] = array(
	'dsn'	=> '',
	'hostname' => 'localhost',
	'username' => 'root',
	'password' => 'root',
	'database' => 'phpdasar',
	'dbdriver' => 'mysqli',
	'dbprefix' => '',
	'pconnect' => FALSE,
	'db_debug' => (ENVIRONMENT !== 'production'),
	'cache_on' => FALSE,
	'cachedir' => '',
	'char_set' => 'utf8',
	'dbcollat' => 'utf8_general_ci',
	'swap_pre' => '',
	'encrypt' => FALSE,
	'compress' => FALSE,
	'stricton' => FALSE,
	'failover' => array(),
	'save_queries' => TRUE
    );
    ```

    ### ROUTES.PHP SETUP

    1. open file routes.php
    2. tambahkan value pada beberapa variabel di bawah ini

    ```
    $route['default_controller'] = 'admin';
    ```


