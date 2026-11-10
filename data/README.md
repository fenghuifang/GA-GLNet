# TLS-OCS3D Data

This directory documents the **TLS-OCS3D subset** of TLS-OCS3D. The point-cloud files are distributed as a GitHub Release attachment so that cloning the repository does not require downloading the full dataset package.

## Download

- **[Download TLS_OCS3D (ZIP, approximately 1.06 GB)](https://github.com/kwo279929-svg/TLS-3D/releases/download/tls-ocs3d-area1-v1.0/TLS-OCS3D_Area_1.zip)**
- [Release page](https://github.com/kwo279929-svg/TLS-3D/releases/tag/tls-ocs3d-area1-v1.0)
- [Archive checksum](SHA256SUMS.txt)
- [Per-file manifest](Area_1_manifest.json)

Download the named **TLS-OCS3D_Area_1.zip** asset. GitHub's automatically generated “Source code” archives contain the repository files, not the point-cloud package.

## Contents

| Item | Value |
| :--- | ---: |
| Scan directories | 19 |
| Original text files | 887 |
| Point rows | 70,792,140 |
| Uncompressed size | 3,373,047,024 bytes |
| ZIP size | 1,060,721,541 bytes |


## File organization

Extract the ZIP to obtain the following structure:

```text
Area_1/
├── 1_1/
│   ├── dw001.txt
│   ├── dwg001.txt
│   ├── jyz001.txt
│   ├── other001.txt
│   └── ...
├── 1_2/
├── ...
└── 1_28/
```

The 19 scan identifiers are `1_1`, `1_2`, `1_4`, `1_5`, `1_7`, `1_8`, `1_10`, `1_11`, `1_13`, `1_14`, `1_16`, `1_17`, `1_19`, `1_20`, `1_22`, `1_23`, `1_25`, `1_26`, and `1_28`. Gaps in the numbering are retained from the source data.

Text files contain whitespace-separated point records with four columns:

```text
x y z intensity
```

The line above describes the columns; it is not a header stored in the files. No numeric class-ID column is added. Original filename prefixes are retained: `dw`, `dwg`, `dwq`, `dx`, `dz`, `gd`, `gm`, `jcx`, `jyz`, `ls`, `other`, `pwb`, `se`, `xwb`, `zcg`, `zj`, and `zz`. Do not treat alphabetical filename order as a semantic class-ID mapping.

## Verify the download

Expected SHA-256 for `TLS-OCS3D_Area_1.zip`:

```text
a38b71210652d078fc0ed0a7685d6f81892f8fbee86a09edf9551fc90c529e69
```

**Windows PowerShell:**

```powershell
Get-FileHash -Algorithm SHA256 .\TLS-OCS3D_Area_1.zip
Expand-Archive -LiteralPath .\TLS-OCS3D_Area_1.zip -DestinationPath .\TLS-OCS3D
```

**Linux** (place `SHA256SUMS.txt` beside the ZIP):

```bash
sha256sum -c SHA256SUMS.txt
unzip TLS-OCS3D_Area_1.zip -d TLS-OCS3D
```

The [manifest](Area_1_manifest.json) records the relative path, byte size, point-row count, and SHA-256 checksum of every file. Before publication, all archived file contents were checked against their source-file hashes.

[Back to the project overview](../README.md)
