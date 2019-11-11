# alpine-laravel-apache
# This is a short list of the operations that I made in the Dockerfile

    First of all, I base everything on a PHP image, based on alpine distribution.
    I copy all of my Laravel source code on /home/application
    I set the document root to my public Laravel folder
    Request the installation of the operative system packages via apk (all of them were required for my Laravel application). A full list of the available packages can be found on http://dl-cdn.alpinelinux.org/alpine/edge/community/x86_64/
    Extend permissions on the storage folder
    Change the owner of the whole /home/application/ folder
    Enable all the needed modules (different modules could be required, depending of the application)
    Change the document root in the httpd.conf file
    Enable the AllowOverride All instruction
    Enable the pdo_mysql extension (otherwise commands will not be able to access mysql)
    Clean the cache of the packaging system
    Run httpd

Using this Dockerfile, it's now possible to run all of the Laravel Web Applications, it will just be a matter of copying the application source code in /home/application/

Ambiente para aplicaciones basdas en el framework laravel con dependencias como node, perl, ruby integradas.
