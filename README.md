# MVC Light v1

This project was done on educational purpose. 

## Development process

### TODO plan:
- add postgres database class

### Notes:
1. Develop Javascript and CSS in /assets/css_src and /assets/js_src folders. In templates must be links pointing at /assets/css and /assets/js. Updater class will automatically minify your code and move to those folders

2. The only file in core which should be modified is model.php. You colud put there some general constants, as menu pages info. Modifications of other files are not supposed by default.

3. Page creating is done in two steps:
    - Create controller by template "controller_*PAGE_NAME*"(low letters). Put there     class Controller_\*PAGE_NAME*, which       extends controller. If you want just template     rendering leave it empty.
    - Create model file. Naming rules are generally the same as in 'a'. Then, create     there method named 'get_*PAGE_NAME*',      which must return array of values which will     be used in Twig.

4. For non-standart routing create another action_index() in current controller. Sample - controller_ajax.php

5. Ajax is proceed on /ajax/\** address. Naming rules are same. Method, started by default is named action(). It must fill $this->message and that's all. Be carefull - it's not expected to return something.

## Installation:

- Just unzip

### Requirements:

 1. PHP 5 support
 
 2. Mysql supporting mysqli interface
 
 3. Apache2

### Notes:

1. Folder /assets/css_src must have r/w permissions for Apache2 default user.

2. Folder /assets/css/ must have r/w permissions for Apache2 default user

3. Same for /assets/js and /assets/js_src

4. Override option must be allowed for root folder

5. Twig cache folder must has r/w permissions. By default, cache is turned off.

--

Sample project: https://github.com/PhantomOfTheOpera/igronet.alterschool/  