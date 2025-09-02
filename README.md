## Kratos (Fork) – Internal README

This is our maintained fork of Ory Kratos. We keep a tight control over what we ship and when we ship it.

### Goals

- Manage our own Docker image builds
- Selectively include upstream changes
- Add fork-specific changes when needed

### Upstream

- Source: `https://github.com/ory/kratos`
- Sync policy: Periodic manual sync; we may cherry-pick or defer changes

### Docker images

- CI builds/pushes are handled by `.github/workflows/build-push.yml`.
- Local build/push:

```bash
make docker
# or
docker build -f .docker/Dockerfile-alpine -t <your-registry>/kratos:<tag> .
docker push <your-registry>/kratos:<tag>
```

### Documentation

- Upstream product docs and API: see `https://www.ory.sh/kratos/docs/`.
- We archived the original upstream README at `docs/UPSTREAM-README.md`.

### Contributing

- Open fork-specific PRs here. When appropriate, also contribute upstream.
