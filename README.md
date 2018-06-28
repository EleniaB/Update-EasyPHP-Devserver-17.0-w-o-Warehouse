# Update EasyPHP Devserver 17.0 w/o Warehouse
## PHP & xdebug
1. Find and download latest PHP on official site: [PHP site](https://windows.php.net/download "PHP site")
2. **PHP** version for EasyPHP **must be x86 / Thread safe**
e.g. *php-7.2.7-Win32-VC15-x86.zip*
3. Inside *EasyPHP_folder\eds-binaries\php* create a new folder with name corresponding to downloaded php in format „php[version][compiler][platform][actual date: yymmddhhmmss]“ e.g. *php727vc15x86182806115837/*
4. Copy the content of downloaded PHP package into pre-created folder. 
5. Download the xdebug for your version of php from this site: [xdebug site](https://xdebug.org/download.php "xdebug site")
e.g. *php_xdebug-2.7.0alpha1-7.2-vc15.dll*
6. Copy downloaded .dll file into your new php folder
7. From older php folder *php713vc14x86x…/* copy this files:
-- eds-app-actions.php
-- eds-app-dashboard.php
-- eds-app-settings.php
-- php7apache2_4.dll
-- php.ini
8. Open eds-app-settings.php and modify this lines (by your downloaded php/xdebug):
    'app_version' => "7.2.7 x86",
    'app_version_nb' => "7.2.7",
    'app_build' => "VC15",
    'xdebug_version' => "2.7.0",
    'xdebug_dll' => "php_xdebug-2.7.0alpha1-7.2-vc15.dll"
9. Enjoy the newest version of PHP
------------

## phpMyAdmin
1. Download the most recent version of phpMyAdmin from official site: [phpMyAdmin site](https://www.phpmyadmin.net/downloads/ "phpMyAdmin site")
e.g. *phpMyAdmin-4.8.2-all-languages.zip*
2. Copy the content of downloaded archive to *EasyPHP_folder\eds-modules\* 
3. **Delete *setup* ** subfolder
4. From older phpMyAdmin folder inside eds-modules folder copy these files
-- config.inc
-- eds-module.php
5. Open *eds-module.php* and in *$module_info* array replace version, installation  date and folder name on each required places (5x)
6. Enjoy the newest version of phpMyAdmin
