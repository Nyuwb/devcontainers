## Description

Create a `php-fpm` container and a `mysql` for Symfony.  
Lines 14 and 17 are commented because on the first build on an empty project, it will crash the container build.  

Of course, this devcontainer can be used outside of Symfony, just remove the `symfony` feature.

| Container | Version |
|-|-|
| *php-fpm* | 8.3.11 |
| *mysql* | 9.0.1 |
| *composer* | 2.7.9 |
| *node* | 20.17.0 |
