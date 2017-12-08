
## NORME
http://eilgin.github.io/php-the-right-way/
https://github.com/dseguy/clearPHP
https://phpbestpractices.org

## SECURITY
http://phpsecurity.readthedocs.io/en/latest/index.html
http://securingphp.com

## LISTS
https://github.com/ziadoz/awesome-php

## BEST
http://php-di.org/doc/frameworks/slim.html

## ASYNCRONOUS ASYNCRONOUS
https://amphp.org


## CQRS / DDD / EventSourcing
https://github.com/real34/cqrs-es-camboui
https://gist.github.com/jsor/6e79afb989c866915f20
http://martinfowler.com/eaaDev/EventSourcing.html
http://cqrs.nu/
https://dddcommunity.org/resources/ddd_terms/

## XAMPP
xampp multiple !: 
http://webdevzoom.com/install-run-multiple-xampp-windows/


## ENV
https://www.ekito.fr/people/setup-a-development-configuration-for-angularjs-and-a-php-mysql-rest-server-solving-the-cors-issue/

## SSO
https://github.com/jasny/sso
http://stackoverflow.com/questions/4061537/best-way-to-implement-single-sign-on-with-all-major-providers


## IMAGE
https://github.com/eventviva/php-image-resize

## OAUTH2
https://github.com/akrabat/slim-bookshelf-api
https://speakerdeck.com/akrabat/2017-04-08-phpyorkshire-slim-oauth2

## COMPOSER
composer dump-autoload (GENERATE import class)
composer update (update dependecies & generate import class)


## MYSQL REGEXP
https://github.com/hholzgra/mysql-udf-regexp/tree/master/regexp


## XAMPP INCLUDE html pages

c:/xampp/apache/conf/httpd.conf
Search for:
AddType text/html .shtml
Add the below two lines:
AddType text/html .html
AddOutputFilter INCLUDES .html
Go to Xampp Control Panel and stop the session and restart again.
Refresh the page in browser and see, the virtual includes will start working.



<!--#include virtual="/fr/header.html" -->
<!--#include virtual="/se/site/as-html-web/site/fr/header.html" -->