FROM splitbrain/phpfarm:jessie

RUN apt-get update && apt-get install -y git

COPY --from=composer:latest /usr/bin/composer /usr/bin/composer
COPY . /var/www/

WORKDIR /var/www/

RUN curl -LSs https://box-project.github.io/box2/installer.php | php-5.3 && cp box.phar /usr/bin/box
