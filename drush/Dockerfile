FROM ubuntu:trusty

RUN apt-get update && apt-get install -y wget php5  \
    && wget http://ftp.drupal.org/files/projects/drush-All-Versions-2.1.tar.gz \
    && tar -xzf drush-All-Versions-2.1.tar.gz \
    && chmod a+x /drush/drush \
    && ln -s /drush/drush /usr/bin/drush

WORKDIR /opt
RUN wget http://download.pear.php.net/package/Console_Table-1.1.4.tgz \
    && tar -xzf Console_Table-1.1.4.tgz \
    && cp Console_Table-1.1.4/Table.php /drush/includes/table.inc \
    && chmod a+r /drush/includes/table.inc


