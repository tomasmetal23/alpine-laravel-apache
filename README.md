# alpine-laravel-apache
# This is a short list of the operations that I made in the Dockerfile

1. First of all, I base everything on a PHP image, based on alpine distribution.
1. I copy all of my Laravel source code on /home/application
1. I set the document root to my public Laravel folder
1. Request the installation of the operative system packages via apk (all of them were required for my Laravel application). A full list of the available packages can be found on http://dl-cdn.alpinelinux.org/alpine/edge/community/x86_64/
1. Extend permissions on the storage folder
1. Change the owner of the whole /home/application/ folder
1. Enable all the needed modules (different modules could be required, depending of the application)
1. Change the document root in the httpd.conf file
1. Enable the AllowOverride All instruction
1. Enable the pdo_mysql extension (otherwise commands will not be able to access mysql)
1. Clean the cache of the packaging system
1. Run httpd

Using this Dockerfile, it's now possible to run all of the Laravel Web Applications, it will just be a matter of copying the application source code in /home/application/

Ambiente para aplicaciones basadas en el framework laravel con dependencias como node, perl y ruby integradas.
