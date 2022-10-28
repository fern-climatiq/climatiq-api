# Climatiq API

Tagging a release on this repository will update the:

- [TypeScript SDK Github Repo](https://github.com/fern-climatiq/climatiq-node)
- [Java SDK Github Repo](https://github.com/fern-climatiq/climatiq-java)
- [OpenAPI Description Github Repo](https://github.com/fern-climatiq/climatiq-openapi)
- _More SDKs to come..._

## What is in this repository?

This repository contains

- Climatiq's Fern API Definition which lives in the [definition](./fern/api/definition/) folder
- Generators (see [generators.yml](./fern/api/generators.yml))

## What is in the API Definition?

The API Definition contains information about what endpoints, types, and errors are used in the API. The definition is broken into smaller files such as [estimate.yml](fern/api/definition/estimate.yml) and [flights.yml](fern/api/definition/flights.yml).

In order to make sure that the definition is valid, you can use the Fern CLI.

```bash
npm install -g fern-api # Installs CLI
fern check # Checks if the definition is valid
```

## What are Generators?

Generators read in your API Definition and output files or code (i.e. the TypeScript SDK Generator) and are tracked in [generators.yml](./fern/api/generators.yml).

To trigger the generators run:

```bash
fern release <version>
```

This command currently runs in a GitHub workflow (see [ci.yml](.github/workflows/ci.yml#L32))
