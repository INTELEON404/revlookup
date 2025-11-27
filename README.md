# RevLookup

```
┏━┓┏━╸╻ ╻╻  ┏━┓┏━┓╻┏ ╻ ╻┏━┓
┣┳┛┣╸ ┃┏┛┃  ┃ ┃┃ ┃┣┻┓┃ ┃┣━┛
╹┗╸┗━╸┗┛ ┗━╸┗━┛┗━┛╹ ╹┗━┛╹
```

**Fast, clean, multi-threaded reverse DNS lookup tool** – built for pure output and maximum usability.  
No banners during scan (optional), no verbose noise. Just hostnames.

**Original concept:** [HunterDep](https://github.com/yHunterDep).
**Fully rewritten, optimized by:** [INTELEON404](https://github.com/INTELEON404)  
**Current version:** **2.3** (November 2025)  
**Language:** Python 3.6+  

[![Python 3.6+](https://img.shields.io/badge/python-3.6%2B-blue)](https://www.python.org/downloads/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## Highlights

| Feature                     | RevLookup v2.3                          |
|-----------------------------|-----------------------------------------|
| Threading                   | Up to **5000** concurrent threads       |
| Output                      | Hostnames only (clean)                  |
| Input types                 | IP • Domain • CIDR • File (mixed)       |
| Unique filtering            | `-u` (optional)                         |
| File output                 | `-o filename`                           |
| Banner                      | Shown by default • disable with `--silent` |
| Dependencies                | Standard library + `pyfiglet` only      |

## Features

- Blazing-fast multi-threaded reverse DNS lookups
- Flexible thread control (`-td N`, max 5000)
- Supports single targets, full CIDR ranges, or mixed input files
- Optional unique hostname deduplication
- Zero bloat – lightweight and dependency-minimal
- Clean, distraction-free output

## Installation

### Option 1: Clone the repository
```bash
git clone https://github.com/INTELEON404/RevLookup.git
cd RevLookup
chmod +x revlookup
sudo mv revlookup /usr/local/bin/
```

### Option 2: One-liner (single file)
```bash
wget https://raw.githubusercontent.com/INTELEON404/RevLookup/main/revlookup -O revlookup
chmod +x revlookup
sudo mv revlookup /usr/local/bin/
```

**Requirements:** Python 3.6 or higher

## Usage Examples

```bash
# Single IP or domain
revlookup -t google.com
revlookup -t 1.1.1.1

# Full CIDR range
revlookup -c 13.35.0.0/16

# From file (supports mixed IPs/domains/CIDRs)
revlookup -f targets.txt

# Max performance + unique results + save output
revlookup -f targets.txt -u -td 4000 -o hostnames.txt

# No banner (quiet mode)
revlookup -t 8.8.8.8 --silent
```

### Full Help Menu
```bash
revlookup -h
```

```
usage: revlookup (-t TARGET | -f FILE | -c CIDR) [-o OUTPUT] [-u] [-td N] [--silent] [-h]

options:
  -t, --target TARGET      Single IP or domain
  -f, --file FILE          File with targets (one per line)
  -c, --cidr CIDR          CIDR range (e.g. 192.168.0.0/16)
  -o, --output OUTPUT      Save results to file
  -u, --unique             Output only unique hostnames
  -td, --threads N         Number of threads (default: 1000, max: 5000)
  --silent                 Suppress banner
  -h, --help               Show this help message and exit
```

## Example Output

```bash
$ revlookup -t google.com

┏━┓┏━╸╻ ╻╻  ┏━┓┏━┓╻┏ ╻ ╻┏━┓
┣┳┛┣╸ ┃┏┛┃  ┃ ┃┃ ┃┣┻┓┃ ┃┣━┛
╹┗╸┗━╸┗┛ ┗━╸┗━┛┗━┛╹ ╹┗━┛╹

hkg07s52-in-f14.1e100.net
lga34s22-in-f4.1e100.net
syd09s23-in-f14.1e100.net
fra16s62-in-f14.1e100.net
mad08s15-in-f3.1e100.net
```

## Contributing

Pull requests are welcome! For major changes, please open an issue first.

## License

[MIT License](LICENSE) © 2025 INTELEON404

---

**Star this repo if you find it useful!** 🚀  
GitHub: https://github.com/INTELEON404/RevLookup
