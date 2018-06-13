# newman-reporter-statsd
A [newman](https://github.com/postmanlabs/newman) reporter for StatsD.  See the [newman documentation](https://www.getpostman.com/docs/postman/collection_runs/command_line_integration_with_newman) for more info. Inspired by [newman-reporter-teamcity](https://github.com/leafle/newman-reporter-teamcity).

## Getting Started

1. Install `newman`
2. Install `newman-reporter-statsd`

### Prerequisites

1. StatsD
2. [npm](https://www.npmjs.com/)
3. `newman`

```
npm install -g newman
```

### Installing

Install with npm

```
npm install -g newman-reporter-statsd
```

### Usage

- The `-r statsd` is the flag to enable StatsD reporting.

- The `--reporter-statsd-destination <ip-address>` is the flag to set destination ip address.

- The `--reporter-statsd-port <port-number>` is the flag to set destination port.

```
newman run <collection-url> -r statsd --reporter-statsd-destination <ip-address> --reporter-statsd-port <port-number>
```

Optional:

- The `-e <environment-url>` is the flag to optionaly add environment.

Note:

- Flags `<collection-url` and `<environment-url>` could be path to *.json files exported from Postman App in your file system or url to public Collection.

The output will be sent to StatsD via UDP.
