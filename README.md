```markdown
# RevLookup v3.9 — Pure • Fast • Silent • Elite

```
┏━┓┏━╸╻ ╻╻  ┏━┓┏━┓╻┏ ╻ ╻┏━┓
┣┳┛┣╸ ┃┏┛┃  ┃ ┃┃ ┃┣┻┓┃ ┃┣━┛
╹┗╸┗━╸┗┛ ┗━╸┗━┛┗━┛╹ ╹┗━┛╹  
```

**Dev By:** HunterDep  
**Mod By:** INTELEON404  
**GitHub:** https://github.com/INTELEON404

The fastest, cleanest and most beautiful reverse DNS lookup tool ever made.  
Zero bloat. Only resolved hostnames. Pure output.

---

### Features

- Lightning-fast multi-threaded reverse lookups (up to 5000 threads)
- Accepts **IP** or **domain name**
- Full **CIDR** support
- Load targets from **file** (IPs, domains, CIDRs)
- `-u / --unique` → deduplicate results instantly
- `-td N` → control thread count (default: 1000)
- `-o` → save results to file
- Pure output — **only hostnames**, nothing else
- Beautiful ASCII art + clean help menu

---

### Installation

```bash
git clone https://github.com/INTELEON404/RevLookup.git
cd RevLookup
chmod +x revlookup
```

Or just copy the single file:

```bash
wget https://raw.githubusercontent.com/INTELEON404/RevLookup/main/revlookup
chmod +x revlookup
```

---

### Usage

```bash
# Single target
./revlookup -t google.com

# CIDR range
./revlookup -c 1.1.1.0/24

# From file (supports IPs, domains, CIDRs)
./revlookup -f targets.txt

# Unique results only + custom threads + save output
./revlookup -f targets.txt -u -td 2000 -o resolved_hosts.txt
```

### Help Menu

```bash
./revlookup -h
```

```
usage: revlookup (-t TARGET | -f FILE | -c CIDR) [-o OUTPUT] [-u] [-td N] [-h]

RevLookup v3.9 — Pure Results Only

options:
  -t, --target TARGET     Single IP or domain
  -f, --file FILE         File with targets
  -c, --cidr CIDR         CIDR range
  -o, --output OUTPUT     Save results to file
  -u, --unique            Show only unique hostnames
  -td, --threads N        Max threads (default: 1000)
  -h, --help              show this help message and exit
```

---

### Example Output

```bash
$ ./revlookup -t google.com

┏━┓┏━╸╻ ╻╻  ┏━┓┏━┓╻┏ ╻ ╻┏━┓
┣┳┛┣╸ ┃┏┛┃  ┃ ┃┃ ┃┣┻┓┃ ┃┣━┛
╹┗╸┗━╸┗┛ ┗━╸┗━┛┗━┛╹ ╹┗━┛╹  

hkg07s52-in-f14.1e100.net
lga34s22-in-f4.1e100.net
syd09s23-in-f14.1e100.net
fra16s62-in-f14.1e100.net
...
```

---

### Made for hunters. Used by legends.

**INTELEON404** — BeHunt Elite | 2025
```
