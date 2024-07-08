## Description

Create a `php-fpm` container and a `mysql` for Symfony.  
Lines 14 and 17 are commented because on the first build on an empty project, it will crash the container build.  

Of course, this devcontainer can be used outside of Symfony.

| Container | Version |
|-|-|
| *php-fpm* | 8.3.9 |
| *mysql* | 8.0.38 |