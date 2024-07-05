## Description

Create a `php-fpm` container for Symfony, without any database.  
Lines 22 and 25 are commented because on the first build on an empty project, it will crash the container build.  

Of course, this devcontainer can be used outside of Symfony.

| Container | Version |
|-|-|
| *php-fpm* | 8.3.8 |