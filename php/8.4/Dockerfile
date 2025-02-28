FROM cimg/php:8.3
RUN wget -O /tmp/doctl.tar.gz https://github.com/digitalocean/doctl/releases/download/v1.121.0/doctl-1.121.0-linux-amd64.tar.gz && tar xzf /tmp/doctl.tar.gz -C /tmp && sudo mv /tmp/doctl /usr/local/bin/doctl
RUN wget -O /tmp/sentry-cli https://github.com/getsentry/sentry-cli/releases/download/2.42.2/sentry-cli-Linux-x86_64 && sudo mv /tmp/sentry-cli /usr/local/bin/sentry-cli && sudo chmod 0755 /usr/local/bin/sentry-cli
