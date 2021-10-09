FROM cimg/php:7.4
ENV PATH="export PATH=~/.composer/vendor/bin:${PATH}"
RUN composer global require deployer/deployer:6.8.0
RUN wget -O /tmp/doctl.tar.gz https://github.com/digitalocean/doctl/releases/download/v1.65.0/doctl-1.65.0-linux-amd64.tar.gz && tar xzf /tmp/doctl.tar.gz -C /tmp && sudo mv /tmp/doctl /usr/local/bin/doctl
RUN wget -O /tmp/sentry-cli https://downloads.sentry-cdn.com/sentry-cli/1.69.1/sentry-cli-Linux-x86_64 && sudo mv /tmp/sentry-cli /usr/local/bin/sentry-cli && sudo chmod 0755 /usr/local/bin/sentry-cli
