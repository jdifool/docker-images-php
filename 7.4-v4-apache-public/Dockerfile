ARG PHP_EXTENSIONS="exif gd imagick imap intl ldap sockets tidy uploadprogress uuid xmlrpc xsl yaml"

FROM thecodingmachine/php:7.4-v4-apache

ENV APACHE_DOCUMENT_ROOT=public/ \
	PHP_INI_ALWAYS_POPULATE_RAW_POST_DATA=-1 \
	PHP_INI_MAX_EXECUTION_TIME=240 \
	PHP_INI_MAX_INPUT_VARS=1500 \
	PHP_INI_UPLOAD_MAX_FILESIZE=32M \
	PHP_INI_POST_MAX_SIZE=32M \
	TZ=Europe/Berlin

RUN sudo apt-get update && \
	sudo apt-get install -y --no-install-recommends imagemagick && \
	sudo rm -rf /var/lib/apt/lists/*
