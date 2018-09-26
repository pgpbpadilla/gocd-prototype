# GoCD example

Runs a basic setup for GoCD using two containers:

- Agent
- Server


# Requirements

- Docker + Docker compose

# Quick start

- `./start.sh` - Start containers
- `./stop.sh` - Stop all containers
- `./clean.sh` - Delete all data directories

# Pipelines as code

- [Sample YAML pipeline](https://docs.gocd.org/current/advanced_usage/pipelines_as_code.html#storing-pipeline-configuration-in-yaml`)

# To Do

- Setup an example of pipeline as code
- Best practices:
    - Config XML size and multiple projects
        - https://github.com/gocd/gocd/issues/838
    - Version control Config XML
        - https://github.com/gocd/gocd/issues/1133

# Gotchas

- Even though the agent is registered successfully with this setup, it won't
start processing pipelines until it's enabled:
    - Agents Nav Item
    - Select agent
    - Click the Enable option

## Pipelines as code

- Sometimes the YAML plugins does not load correctly. Simply restart.
    - You can see the Plugins that were loaded under Admin>Plugins