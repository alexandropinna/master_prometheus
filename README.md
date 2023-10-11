# Monitoring Stack with Docker Compose

This project defines a monitoring stack using Docker Compose, which includes the following tools:

- **Prometheus**: Monitoring and alerting toolkit.
- **Grafana**: Analytics and monitoring platform.
- **Alertmanager**: Handles alerts sent by client applications such as Prometheus.
- **Node Exporter**: Exports system metrics.
- **cAdvisor**: Provides resource usage and performance characteristics of running containers.
- **Pushgateway**: For batch job metrics.
- **Loki**: A horizontally scalable, highly available, multi-tenant log aggregation system.
- **Promtail**: Log agent for Loki.

## Prerequisites

- Docker
- Docker Compose

## Configuration

1. **Environment Variables**: You can set Grafana credentials via the `ADMIN_USER` and `ADMIN_PASSWORD` environment variables. If not specified, default values (`admin` and `cLaMDjrXrP85giN7` respectively) will be used.

2. **Volumes**: Volumes are defined for data persistence in `prometheus`, `grafana`, `loki`, and `promtail`.

3. **Configurations**: Configuration files for `prometheus`, `grafana`, `alertmanager`, `loki`, and `promtail` should be present in the relative paths specified in the `docker-compose.yml`.

## Usage

1. **Start**:

```bash
docker-compose up -d
```

2. **Stop**:

```bash
docker-compose down
```

## Accessing the Applications

- **Prometheus**: [http://localhost:9090](http://localhost:9090)
- **Grafana**: [http://localhost:3000](http://localhost:3000)
- **Alertmanager**: [http://localhost:9093](http://localhost:9093)
- **cAdvisor**: [http://localhost:8090](http://localhost:8090)
- **Pushgateway**: [http://localhost:9091](http://localhost:9091)
- **Loki**: [http://localhost:3100](http://localhost:3100)



