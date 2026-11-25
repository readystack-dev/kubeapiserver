# Provenance — kube-apiserver (`v1.36.6-CE-ubuntu24.04-r5`)

Every item below is copied from a record in this archive; the record is named in brackets.

## Source

- Upstream repository: https://github.com/kubernetes/kubernetes
- Revision built: `v1.36.6` (commit `1b2171b110bb2a2542e1322035c6583ec86eb976`)
- Source tree: `803692e6a7661d2d72c4cdf0a2a2459bdf6646e2b6c955ed7362f279ee4fa004` over 29206 files [`docs/provenance/SOURCE_TREE_HASH.json`]
- Community Edition only: enterprise code is removed or refused before the build (CE audit at acquire).

## Build

- Method: `source-rebuild-go`; base image `ubuntu:24.04`
- Compiled with `--network=none` from vendored source, dependencies and base images; BuildKit pinned to `moby/buildkit:v0.31.2` (shipped in `toolchain/`).
- SOURCE_DATE_EPOCH: `1795244549` [`SOURCE_DATE_EPOCH.txt`]
- Frozen inputs: [`docs/provenance/FREEZE_MANIFEST.json`], build recipe: [`docs/provenance/BUILD_RECIPE.json`].

## Output

- Published image: `readystack/kubeapiserver:v1.36.6-CE-ubuntu24.04-r5` — index digest `sha256:3a2e3dc2bafb8e020c473614b630033e31d3f31caac1413480d246dc47501e98` [`docs/provenance/LOCKED_DIGEST.txt`]
- linux/amd64 image digest `sha256:3d0295d9d441a02aefb75dac3ccc5d09c3c9d34cbcec761426a3e9af6c8841cf` — reproduced from this archive before publishing [`docs/provenance/REPRO_VERIFICATION.json`].

## Attestations and signature

- SBOM + SLSA provenance attached to the image: attached: an SPDX SBOM and SLSA v1 provenance [`docs/provenance/SCOUT_VERDICT.json`]
- cosign signature by the ReadyStack release key: verified before publishing. Check it: `cosign verify --key https://readystack.dev/keys/cosign.pub readystack/kubeapiserver:v1.36.6-CE-ubuntu24.04-r5`

## Pinned inputs, and why

- 31 pinned inputs, each with where it came from, why this one, how it was checked and when it was decided: `docs/PINS.md` [`docs/provenance/PINS.json`] (upstream source 2, base and build images 3, image digests 2, dependency versions readystack sets 16, components from other repositories 1, pins in the kit's dockerfiles 3, readystack's build engine 1, dependencies upstream chose 2, services the release checks run beside 1).

## Build trail

- How this release passed through the ReadyStack harness, record by record (every chain, drive, stage, review round, defect and check, each naming the record it is copied from): `ReadyStack-kubeapiserver-v1.36.6-CE-ubuntu24.04-r5.trail.json`, published beside this archive and signed with the release key (`ReadyStack-kubeapiserver-v1.36.6-CE-ubuntu24.04-r5.trail.json.sigstore`), and readable at https://readystack.dev/products/kubeapiserver/trail/v1.36.6-CE-ubuntu24.04-r5.

