# haproxy-prometheus-grafana
HAProxy+Prometheus+Grafana

This repo contains the Docker Compose config to test the integration between HAProxy, Grafana and Prometheus.

It has a very simple configuration for haproxy under haproxy_config. It has defined one frontend, one backend with two servers and enabled stats with authentication.
There is a haproxy-exporter running retriving data from haproxy usin basic auth. Also there is a node exporter getting node statistics and sending it to prometheus.

Grafana is used  to display metrics, with preconfigured HAProxy and prometheus dashboards, and preconfigured datasource to gather data from prometheus.

To execute it just run docker-compose up on the root of the directory.