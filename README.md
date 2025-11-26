# RevLookup

```
┏━┓┏━╸╻ ╻╻ ┏━┓┏━┓╻┏ ╻ ╻┏━┓
┣┳┛┣╸ ┃┏┛┃ ┃ ┃┃ ┃┣┻┓┃ ┃┣━┛
╹┗╸┗━╸┗┛ ┗━╸┗━┛┗━┛╹ ╹┗━┛╹
```

**The fastest, cleanest, and most beautiful reverse DNS lookup tool ever made.**  
Zero bloat. Only resolved hostnames. Pure output.

**Original by:** HunterDep  
**Maintained & Enhanced by:** INTELEON404  
**GitHub:** https://github.com/INTELEON404/RevLookup

---

### Features

- ⚡ **Blazing fast** multi-threaded reverse lookups (up to **5000 threads**)
- Accepts **single IP**, **domain name**, or **full CIDR ranges**
- Load targets from **file** (supports mixed IPs, domains, and CIDRs)
- `-u / --unique` → instant deduplication of results
- `-td N` → fully customizable thread count (default: 1000)
- `-o` → save output to file
- **Pure output mode** — only resolved hostnames, no noise
- Beautiful ASCII banner & clean help menu

---

### Installation

#### Option 1: Clone the repo
```bash
git clone https://github.com/INTELEON404/RevLookup.git
cd RevLookup
chmod +x revlookup
```

#### Option 2: One-liner (single file)
```bash
wget https://raw.githubusercontent.com/INTELEON404/RevLookup/main/revlookup -O revlookup
chmod +x revlookup
```

---

### Usage Examples

```bash
# Single target (IP or domain)
./revlookup -t google.com

# Scan entire CIDR range
./revlookup -c 1.1.1.0/24

# Load targets from file (IPs, domains, CIDRs supported)
./revlookup -f targets.txt

# Unique results + 2000 threads + save output
./revlookup -f targets.txt -u -td 2000 -o resolved_hosts.txt

# Show help
./revlookup -h
```

---

### Help Menu

```bash
usage: revlookup (-t TARGET | -f FILE | -c CIDR) [-o OUTPUT] [-u] [-td N] [-h]

RevLookup v3.9 — Pure Results Only

options:
  -t, --target TARGET     Single IP or domain
  -f, --file FILE         File containing targets (one per line)
  -c, --cidr CIDR         CIDR range (e.g., 192.168.1.0/24)
  -o, --output OUTPUT     Save results to file
  -u, --unique            Show only unique hostnames
  -td, --threads N        Max threads (default: 1000, max: 5000)
  -h, --help              Show this help message and exit
```

---

### Example Output

```bash
$ ./revlookup -t google.com
┏━┓┏━╸╻ ╻╻ ┏━┓┏━┓╻┏ ╻ ╻┏━┓
┣┳┛┣╸ ┃┏┛┃ ┃ ┃┃ ┃┣┻┓┃ ┃┣━┛
╹┗╸┗━╸┗┛ ┗━╸┗━┛┗━┛╹ ╹┗━┛╹

hkg07s52-in-f14.1e100.net
lga34s22-in-f4.1e100.net
syd09s23-in-f14.1e100.net
fra16s62-in-f14.1e100.net
mad08s15-in-f3.1e100.net
...
```

---

**Made for hunters. Used by legends.**

**INTELEON404** — BeHunt Elite | 2025  
https://github.com/INTELEON404/RevLookup

