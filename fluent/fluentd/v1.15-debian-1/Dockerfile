FROM fluent/fluentd:v1.15-debian-1

# Use root account to use apt
USER root

# below RUN includes plugin as examples elasticsearch is not required
# you may customize including plugins as you wish
RUN gem uninstall -I elasticsearch && gem install elasticsearch -v 8.3.2
RUN ["gem", "install", ""]

COPY fluent.conf /fluentd/etc/
# COPY entrypoint.sh /bin/

USER fluent