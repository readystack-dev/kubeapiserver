# kube-apiserver: ReadyStack build kit

The offline build kit for the Docker image `readystack/kubeapiserver:v1.36.6-CE-ubuntu24.04-r5`. It holds what the image is built from (upstream source, base images, toolchain, pinned dependencies) and the documents, so the image can be rebuilt with no network access (`docker build --network=none`).

- Release: [v1.36.6-CE-ubuntu24.04-r5](https://github.com/readystack-dev/kubeapiserver/releases/tag/v1.36.6-CE-ubuntu24.04-r5)
- Image: [`docker.io/readystack/kubeapiserver:v1.36.6-CE-ubuntu24.04-r5`](https://hub.docker.com/r/readystack/kubeapiserver/tags), manifest digest `sha256:3d0295d9d441a02aefb75dac3ccc5d09c3c9d34cbcec761426a3e9af6c8841cf`
- Product page: https://readystack.dev/products/kubeapiserver
- Defects: this repository's Issues (defects recorded from 25 November 2026 on) and https://readystack.dev/defects.html?product=kubeapiserver

kube-apiserver is distributed under its upstream licence (Apache-2.0); the kit contains upstream's source under that licence, and each vendored component under its own.

## Download

From the [v1.36.6-CE-ubuntu24.04-r5 release](https://github.com/readystack-dev/kubeapiserver/releases/tag/v1.36.6-CE-ubuntu24.04-r5): `ReadyStack-kubeapiserver-v1.36.6-CE-ubuntu24.04-r5.tar.gz` (501.4 MB), SHA-256 `4842b8ce14bc5ab304896a4bab11c47f5198b4ad6b07b19bfb2b028586dcfef7`.

```sh
sha256sum --check --ignore-missing SHA256SUMS
```

## Verify and rebuild

The rebuild statement is signed with the ReadyStack release key. Check the signature before you rely on it:

```sh
cosign verify-blob --key https://readystack.dev/keys/cosign.pub \
  --bundle ReadyStack-kubeapiserver-v1.36.6-CE-ubuntu24.04-r5.rebuild.json.sigstore ReadyStack-kubeapiserver-v1.36.6-CE-ubuntu24.04-r5.rebuild.json
```

Unpack with `-p` so file modes are kept, then follow the kit's own README.md and docs/REBUILD.md:

```sh
tar -xpzf ReadyStack-kubeapiserver-v1.36.6-CE-ubuntu24.04-r5.tar.gz
cd v1.36.6-CE-ubuntu24.04-r5
less README.md docs/REBUILD.md
```

The build trail (`ReadyStack-kubeapiserver-v1.36.6-CE-ubuntu24.04-r5.trail.json`, signed the same way, and its Markdown copy) records how this release was built and checked.

## This repository

`recipe/` holds the kit's recipe files (Dockerfiles, build scripts, pins) as published at https://readystack.dev/products/kubeapiserver/recipe. The complete kit is the release download. Each release is a tag here.
