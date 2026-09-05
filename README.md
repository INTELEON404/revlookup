<div align="center">

<img src="https://github.com/INTELEON404/Template/blob/main/reLookup.png" alt="RevLookup" />

# REVLOOKUP

**Lightweight Reverse DNS / PTR Lookup CLI**

[![Python](https://img.shields.io/badge/Python-3.6%2B-blue)](https://www.python.org/)
[![License](https://img.shields.io/badge/License-MIT-yellow)](LICENSE)

</div>

---

## Overview

RevLookup is a lightweight, multi-threaded **Reverse DNS / PTR lookup** utility written in Python.

It supports:

* IPv4
* IPv6
* Domains
* CIDR ranges
* Mixed target files
* Multi-threaded lookups
* Progress display
* Result file output
* Silent mode

No external dependencies are required.

## Installation

```bash
git clone https://github.com/INTELEON404/revlookup.git
cd revlookup
chmod +x revlookup
sudo cp revlookup /usr/local/bin/
```


Run directly:

```bash
python3 revlookup -t 8.8.8.8
```

## Usage

### IPv4

```bash
revlookup -t 8.8.8.8
```

### IPv6

```bash
revlookup -t 2001:4860:4860::8888
```

### Domain

```bash
revlookup -t google.com
```

### CIDR

```bash
revlookup -c 8.8.8.0/24
```

### Input File

```bash
revlookup -f targets.txt
```

### Custom Threads

```bash
revlookup -f targets.txt -td 500
```

### Save Results

```bash
revlookup -t 8.8.8.8 -o results.txt
```

### Silent Mode

```bash
revlookup -t 8.8.8.8 -s
```

## Options

| Option           | Description                            |
| ---------------- | -------------------------------------- |
| `-t, --target`   | Single IP address or domain            |
| `-f, --file`     | File containing IPs, domains, or CIDRs |
| `-c, --cidr`     | CIDR range                             |
| `-o, --output`   | Save successful results to a file      |
| `-td, --threads` | Number of worker threads               |
| `-s, --silent`   | Disable banner and progress display    |
| `-h, --help`     | Show help message                      |

**Default threads:** `100`
**Maximum threads:** `5000`
**Maximum CIDR expansion:** `65,536` addresses

## Input File

Targets are supplied one per line.

```text
8.8.8.8
1.1.1.1
2001:4860:4860::8888
google.com
8.8.8.0/24
```

Blank lines and lines beginning with `#` are ignored.

## Output

Successful lookups are printed as:

```text
8.8.8.8 -> dns.google
1.1.1.1 -> one.one.one.one
```

With `-o`:

```text
8.8.8.8	dns.google
1.1.1.1	one.one.one.one
```

## Requirements

* Python 3.6+
* No external dependencies
