FROM grafana/grafana:5.0.1
# https://hub.docker.com/r/grafana/grafana/tags/

COPY datasources.yaml /etc/grafana/provisioning/datasources/
COPY providers.yml /etc/grafana/provisioning/dashboards/
COPY dashboards /etc/grafana/dashboards/

ENV GF_SECURITY_ADMIN_PASSWORD=admin \
    GF_SECURITY_ADMIN_USER=admin \
    GF_PATHS_PROVISIONING=/etc/grafana/provisioning/
