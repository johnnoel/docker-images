FROM php:8.4-cli-alpine
ADD --chmod=0755 https://github.com/mlocati/docker-php-extension-installer/releases/latest/download/install-php-extensions /usr/local/bin/
RUN apk add wget openssh-client && install-php-extensions pdo_pgsql intl gd gettext imagick opcache xsl zip @composer
RUN wget -O /tmp/sentry-cli https://github.com/getsentry/sentry-cli/releases/latest/download/sentry-cli-Linux-x86_64 && mv /tmp/sentry-cli /usr/local/bin/sentry-cli && chmod 0755 /usr/local/bin/sentry-cli && \
    wget -O /tmp/hcloud.tar.gz https://github.com/hetznercloud/cli/releases/latest/download/hcloud-linux-amd64.tar.gz && tar xzf /tmp/hcloud.tar.gz -C /tmp && mv /tmp/hcloud /usr/local/bin/hcloud && \
    wget -O /usr/local/bin/b2 https://github.com/Backblaze/B2_Command_Line_Tool/releases/latest/download/b2-linux && chmod 0755 /usr/local/bin/b2
