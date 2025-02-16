PHP-FPM image with frequently-used extensions built in.

Based on Alpine.

Needs volume mounts for the WWW directory, and for the PHP-FPM socket, eg:

    [Container]
    ContainerName=php-wwwmattsnet
    Image=docker.io/cm6051/php84-fpm-heavy:3
    Volume=/home/apache/vhosts/www.matts.net/htdocs:/var/www/html
    Volume=%h/php-wwwmattsnet/:/run/php-fpm/
