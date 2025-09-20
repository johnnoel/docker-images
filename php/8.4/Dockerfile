FROM cimg/php:8.4
ADD --chmod=0755 https://github.com/mlocati/docker-php-extension-installer/releases/latest/download/install-php-extensions /usr/local/bin/
RUN sudo apt update && sudo apt install -y libxslt1-dev && sudo -E install-php-extensions xsl
RUN wget -O /tmp/doctl.tar.gz https://github.com/digitalocean/doctl/releases/download/v1.142.0/doctl-1.142.0-linux-amd64.tar.gz && tar xzf /tmp/doctl.tar.gz -C /tmp && sudo mv /tmp/doctl /usr/local/bin/doctl && \
    wget -O /tmp/sentry-cli https://github.com/getsentry/sentry-cli/releases/download/2.54.0/sentry-cli-Linux-x86_64 && sudo mv /tmp/sentry-cli /usr/local/bin/sentry-cli && sudo chmod 0755 /usr/local/bin/sentry-cli && \
    wget -O /tmp/hcloud.tar.gz https://github.com/hetznercloud/cli/releases/latest/download/hcloud-linux-amd64.tar.gz && tar xzf /tmp/hcloud.tar.gz -C /tmp && sudo mv /tmp/hcloud /usr/local/bin/hcloud
