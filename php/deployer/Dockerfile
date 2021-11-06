FROM php:7.4-cli-alpine
RUN apk add git wget openssh
RUN wget -O /tmp/doctl.tar.gz https://github.com/digitalocean/doctl/releases/download/v1.66.0/doctl-1.66.0-linux-amd64.tar.gz && tar xzf /tmp/doctl.tar.gz -C /tmp && mv /tmp/doctl /usr/local/bin/doctl
RUN wget -O /tmp/sentry-cli https://downloads.sentry-cdn.com/sentry-cli/1.71.0/sentry-cli-Linux-x86_64 && mv /tmp/sentry-cli /usr/local/bin/sentry-cli && chmod 0755 /usr/local/bin/sentry-cli
COPY --from=composer:latest /usr/bin/composer /usr/local/bin/composer
RUN composer global require deployer/deployer:6.8.0
ENV PATH="/root/.composer/vendor/bin:${PATH}"
