FROM circleci/php:8.0-cli
RUN sudo apt-get update && \
sudo apt-get install -y --no-install-recommends libpq-dev libpng-dev libjpeg62-turbo-dev libmagickwand-dev && \
sudo pecl install redis && \
sudo docker-php-ext-configure gd --with-jpeg && \
sudo mkdir -p /usr/src/php/ext/imagick && \
sudo curl -fsSL https://github.com/Imagick/imagick/archive/06116aa24b76edaf6b1693198f79e6c295eda8a9.tar.gz | sudo tar xvz -C "/usr/src/php/ext/imagick" --strip 1 && \
sudo docker-php-ext-install gd pdo_pgsql imagick && \
sudo docker-php-ext-enable redis
RUN wget -O /tmp/doctl.tar.gz https://github.com/digitalocean/doctl/releases/download/v1.61.0/doctl-1.61.0-linux-amd64.tar.gz && tar xzf /tmp/doctl.tar.gz -C /tmp && sudo mv /tmp/doctl /usr/local/bin/doctl
RUN wget -O /tmp/sentry-cli https://downloads.sentry-cdn.com/sentry-cli/1.66.0/sentry-cli-Linux-x86_64 && sudo mv /tmp/sentry-cli /usr/local/bin/sentry-cli && sudo chmod 0755 /usr/local/bin/sentry-cli
