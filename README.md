# Datus Quickstart Data

Small, versioned datasets for Datus quickstart tutorials.

This repository keeps metadata in git and publishes dataset archives as GitHub
Release assets. This keeps clone size small while providing stable download
URLs for tutorials.

## Data Engineering Quickstart

The `data-engineering-v1` release contains:

- `datus-de-lever-quickstart-v1.zip`
- `datus-de-lever-quickstart-v1.zip.sha256`
- `datus-data-engineering-quickstart-stack-v1.zip`
- `datus-data-engineering-quickstart-stack-v1.zip.sha256`

Download and prepare it:

```bash
mkdir -p ~/datus-quickstart-data
cd ~/datus-quickstart-data

curl -L -o datus-de-lever-quickstart-v1.zip \
  https://github.com/Datus-ai/datus-quickstart-data/releases/download/data-engineering-v1/datus-de-lever-quickstart-v1.zip
curl -L -o datus-de-lever-quickstart-v1.zip.sha256 \
  https://github.com/Datus-ai/datus-quickstart-data/releases/download/data-engineering-v1/datus-de-lever-quickstart-v1.zip.sha256
curl -L -o datus-data-engineering-quickstart-stack-v1.zip \
  https://github.com/Datus-ai/datus-quickstart-data/releases/download/data-engineering-v1/datus-data-engineering-quickstart-stack-v1.zip
curl -L -o datus-data-engineering-quickstart-stack-v1.zip.sha256 \
  https://github.com/Datus-ai/datus-quickstart-data/releases/download/data-engineering-v1/datus-data-engineering-quickstart-stack-v1.zip.sha256

shasum -a 256 -c datus-de-lever-quickstart-v1.zip.sha256
shasum -a 256 -c datus-data-engineering-quickstart-stack-v1.zip.sha256
unzip datus-de-lever-quickstart-v1.zip
unzip datus-data-engineering-quickstart-stack-v1.zip

export DACOMP_HOME="$PWD/datus-de-lever-quickstart"
export DATUS_QUICKSTART_STACK="$PWD/datus-data-engineering-quickstart-stack"
cp "$DACOMP_HOME/lever_start.duckdb" "$DACOMP_HOME/lever_workbench.duckdb"
```

## Source

The data is extracted from the public DAComp dataset. See [SOURCE.md](SOURCE.md)
for source, license, and citation details.
