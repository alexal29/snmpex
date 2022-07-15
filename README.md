# snmpex

A sample setup of snmp + exporter + prometheus +grafana

<details>
<summary>Table of Contents</summary>

- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Usage](#usage)
  - [Result Observation](#result-observation)
- [License](#license)

</details>

## Getting Started

### Prerequisites

- Since this repo's script contains some unix command, The best scenario is you are using a Unix-like operating system: macOS, Linux, BSD. On Windows: WSL2 is preferred, but cygwin or msys also mostly work. If you are using other operating system, you can write your own script to run this tool.
- This whole project is built on containerized architect so [Docker](https://docs.docker.com/engine/install/) & [Docker Compose](https://docs.docker.com/compose/install/) should be installed.
- [make](https://www.gnu.org/software/make/) should be installed to be able to run the setup script.

### Usage

```sh
# Run the setup script with the bellow command
make
```

![image](https://user-images.githubusercontent.com/108666941/179147448-41d3ebd6-e1ca-46b1-bfd4-d745d3dff835.png)

### Result Observation

Follow these instructions to view your result.

| How to check           | Method                              |
| ---------------------- | ----------------------------------- |
| Running containers     | `docker compose ps`                 |
| `Prometheus` dashboard | visit http://localhost:9090/        |
| `SNMP` exporter metric | visit http://localhost:9116/metrics |

To implement Grafana graph & chart you need to:

- Create a `Grafana` account
- Create a `Prometheus` data source host on `Grafana`
- Replace `remote_write` info in `prometheus.yml`

## License

snmp is released under the [MIT license](LICENSE.txt).
