# Ansible Role: dedibox-exporter

Provision and manage the Prometheus [dedibox-exporter](https://github.com/FinweVI/dedibox-exporter).  
Exporter to report metrics fetched from the Online.net API.

## Requirements

- Ansible >= 2.8

## Role Variables

All variables which can be overridden are stored in [defaults/main.yml](defaults/main.yml) file as well as in table below.

| Name           | Default Value | Description                        |
| -------------- | ------------- | -----------------------------------|
| `dedibox_exporter_version` | latest | Dedibox Exporter version to install |
| `dedibox_exporter_address` | 127.0.0.1 | Address on which dedibox-exporter listens |
| `dedibox_exporter_port` | 9876 | port on which dedibox-exporter listens |
| `dedibox_exporter_repository ` | github.com/FinweVI/dedibox-exporter | github link to the source code |
| `dedibox_exporter_metric_path` | /metrics | HTTP Route to serve the metrics on |
| `dedibox_exporter_log_level` | 1 | Log Level (0=Debug, 1=Info, 2=Warning, 3=Error, 4=Fatal) |
| `dedibox_exporter_collectors` | [] | List of collector to enable |
| `dedibox_exporter_api_token` | None | Online.net API Token |

See the [defaults/main.yml](defaults/main.yml) file for examples.


## Notes

It's Debian-based Only.
It must be possible to make it CentOS (or any other linux-based OS) compatible.
Issues & PR are welcome for any improvement ;-)

This is heavily inspired by [CloudAlchemy]('https://github.com/cloudalchemy/')
