# Neurosuite apt repository

Source of https://neurosuite.github.io/apt, an apt repository with the `.deb` packages of the
Neurosuite releases for Ubuntu 24.04 (noble) and newer. Setup instructions are on that page.

The [publish workflow](.github/workflows/publish.yml) downloads the `.deb` files attached to the
releases of libneurosuite, NeuroScope, Klusters, NDManager and the NDManager plugins, builds the
repository with `reprepro` and deploys it to GitHub Pages. It runs every night, on pushes to `main`
and by hand. Releases go to the `main` component and pre-releases to `testing`. No packages are
stored in this repository.

The repository is signed with the key in the `APT_SIGNING_KEY` Actions secret. Its public part is
published as `neurosuite.asc`.
