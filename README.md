# alloy-deployments

Examples of Alloy & OTEL Collector deployment configurations used for testing
and research.

## Development

Dependencies:

- `k3d` or `kind`
- `docker`
- `go-task`

## Running this

You'll need to put your secrets in `secrets/` folder. See `Taskfile.yml` and
the `deploy:secrets` step for more information.

Also, the usernames are currently hard-coded in `.alloy` config files. You'll
need to change them to match your environment.

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
