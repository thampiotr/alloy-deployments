# alloy-deployments

Examples of Alloy & OTEL Collector deployment configurations used for testing
and research.

## Development

Dependencies:

- `k3d` or `kind`
- `docker`
- `go-task`
- An OTLP, Loki and Prometheus backends to send data to.

## Running this

You'll need to put your usernames/passwords in `secrets/` folder. See `Taskfile.yml` and
the `deploy:secrets` step for more information. 

    NOTE: that the URLs of endpoints are currently hard-coded.

Example:
```shell
secrets
├── loki_key
├── loki_username
├── mimir_key
├── mimir_username
├── otlp_key
└── otlp_username
```

To run this project:
```shell

# Start a local k3d cluster
$ task k3d:create

# Alternatively, start a local kind cluster
$ task kind:create

# Deploy everything
$ task deploy:all

# See what else you can do
$ task --list
```
