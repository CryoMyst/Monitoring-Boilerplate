# Monitoring Boilerplate with Docker

This boilerplate project provides a comprehensive monitoring setup using Docker Compose. It includes various monitoring services such as Postgres, Loki, Prometheus, Pyroscope, Grafana, and more.

## Quick Start

1. Clone the repository:

    ```
    git clone https://github.com/CryoMyst/Monitoring-Boilerplate
    cd Monitoring-Boilerplate
    ```

2. Update the `.env` file with your desired configurations. Make sure to at least change the following settings for security reasons:

    ```
    POSTGRES_PASSWORD
    GRAFANA_PASSWORD
    NETWORK_NAME
    ```

3. Navigate to the root of the project and spin up the containers:

    ```
    docker-compose up -d
    ```

## Containers

The following containers will be instantiated:

- `postgres`: An object-relational database system that uses and extends the SQL language.
- `loki`: A horizontally-scalable, multi-tenant log aggregation system inspired by Prometheus.
- `prometheus`: An open-source systems monitoring and alerting toolkit.
- `pushgateway`: A metrics cache for Prometheus.
- `pyroscope`: Continuous profiling platform to analyze application performance.
- `grafana`: An open-source platform for monitoring and observability.

## Configuration

Configuration is managed through the `.env` file in the root directory. Before starting up the containers, ensure to modify the defaults, especially the passwords and network name, to ensure a secure setup.

For additional configurations, there's a `config` subdirectory that contains configuration files for the various services.

## Maintenance & Troubleshooting

Logs for each service can be accessed using:
```
docker-compose logs [service-name]
```
Where `[service-name]` is one of `postgres`, `loki`, `prometheus`, `pushgateway`, `pyroscope`, `grafana`.

To stop and remove all containers:
```
docker-compose down
```

## Contribution

Feel free to raise issues or PRs if you find any problems or have improvements in mind.