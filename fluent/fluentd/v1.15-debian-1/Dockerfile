FROM fluent/fluentd:v1.15-debian-1

# Use root account to use apt
USER root

# below RUN includes plugin as examples elasticsearch is not required
# you may customize including plugins as you wish
RUN gem uninstall -I elasticsearch && gem install elasticsearch -v 8.3.0
RUN ["gem", "install", "fluent-plugin-elasticsearch", "--no-document", "--version", "5.2.3"]
RUN ["gem", "install", "fluent-plugin-detect-exceptions", "--no-document", "--version", "0.0.11"]
RUN ["gem", "install", "fluent-plugin-concat", "--no-document", "--version", "2.5.0"]

# COPY fluent.conf /fluentd/etc/
# COPY entrypoint.sh /bin/

USER fluent