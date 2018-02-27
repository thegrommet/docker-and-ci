FROM circleci/php:7.1-apache-node-browsers
RUN sudo apt-get install python-pip
RUN sudo pip install awscli==1.14.38
RUN sudo apt-get install pax
RUN sudo apt-get install mysql-client
RUN sudo apt-get install -y libpng12-dev libicu-dev libxml2-dev libxslt1-dev libmcrypt-dev libcurl4-openssl-dev libmysqlclient-dev libzip-dev libjpeg62-turbo-dev libgif-dev libfreetype6-dev
RUN sudo docker-php-ext-configure gd --with-png-dir=/usr/include/ --with-jpeg-dir=/usr/include/ --with-freetype-dir=/usr/include/
RUN sudo docker-php-ext-install gd
RUN sudo docker-php-ext-install zip pdo_mysql xsl intl bcmath soap mcrypt iconv curl
RUN echo "[PHP]\nmemory_limit=3G\n" | sudo dd of=/usr/local/etc/php/conf.d/0_memory_limit.ini
