# asdf-cogh

asdf plugin that installs `cogh`, the CogniCode installer, from the GitHub
Release assets of [Rubentxu/CogniCode](https://github.com/Rubentxu/CogniCode).
It checks the tarball against the release `SHA256SUMS` and stops on a
mismatch. `cogh` then installs `cognicode` and `cognicode-mcp`
(`cogh install mcp-server --profile reviewer`). Only Linux x86_64 GNU is
published.

```sh
asdf plugin add cogh https://github.com/Rubentxu/asdf-cogh.git
asdf list all cogh
asdf install cogh 0.103.0
asdf set cogh 0.103.0
asdf reshim cogh
"$(asdf which cogh)" --version   # check the path, not only the name
```

No provenance attestation exists for 0.103.0; the checksum proves integrity
against the release manifest only.

The plugin is developed in the CogniCode repository under
`scripts/distribution/asdf-cogh/`, with an offline contract test in
`scripts/ci/test_asdf_cogh_plugin.py`. This repository is its published copy.

Licensed under MIT OR Apache-2.0, at your option.
