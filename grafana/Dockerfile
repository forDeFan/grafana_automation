FROM grafana/grafana:7.1.5-ubuntu

# Disable Login form or not
ENV GF_AUTH_DISABLE_LOGIN_FORM "true"
# Allow anonymous authentication or not
ENV GF_AUTH_ANONYMOUS_ENABLED "true"
# Role of anonymous user, Editor removes help panel also
ENV GF_AUTH_ANONYMOUS_ORG_ROLE "Editor"
# Install plugins separates by comma
ENV GF_INSTALL_PLUGINS="yesoreyeram-infinity-datasource"

# Add provisioning
ADD ./grafana/provisioning /etc/grafana/provisioning
# Add configuration file
ADD ./grafana/grafana.ini /etc/grafana/grafana.ini
# Add dashboard json files
ADD ./grafana/dashboards /etc/grafana/dashboards