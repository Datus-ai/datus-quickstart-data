# Datus Quickstart Data

Small, versioned datasets for Datus quickstart tutorials.

This repository keeps metadata in git and publishes dataset archives as GitHub
Release assets. This keeps clone size small while providing stable download
URLs for tutorials.

## Data Engineering Quickstart

The `data-engineering-v1` release contains:

- `datus-de-lever-quickstart-v1.zip`

Download and prepare it:

```bash
mkdir -p ~/datus-quickstart-data
cd ~/datus-quickstart-data

curl -L -o datus-de-lever-quickstart-v1.zip \
  https://github.com/Datus-ai/datus-quickstart-data/releases/download/data-engineering-v1/datus-de-lever-quickstart-v1.zip

shasum -a 256 datus-de-lever-quickstart-v1.zip
unzip datus-de-lever-quickstart-v1.zip

export DACOMP_HOME="$PWD/datus-de-lever-quickstart"
cp "$DACOMP_HOME/lever_start.duckdb" "$DACOMP_HOME/lever_workbench.duckdb"
```

Expected SHA256:

```text
0e6b83c12c880152c9e29c76959b82f33d36fe2bb82b2c0b4b4d3b3ee2e44dc9  datus-de-lever-quickstart-v1.zip
```

## Source

The data is extracted from the public DAComp dataset. See [SOURCE.md](SOURCE.md)
for source, license, and citation details.
