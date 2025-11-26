# RevLookup

```
┏━┓┏━╸╻ ╻╻  ┏━┓┏━┓╻┏ ╻ ╻┏━┓
┣┳┛┣╸ ┃┏┛┃  ┃ ┃┃ ┃┣┻┓┃ ┃┣━┛
╹┗╸┗━╸┗┛ ┗━╸┗━┛┗━┛╹ ╹┗━┛╹ 
```

**The fastest, cleanest, and most beautiful reverse DNS lookup tool ever made.**  
Zero bloat. Only resolved hostnames. Pure, instant output.

**Original concept & first version:** HunterDep  
**Completely rewritten, optimized & maintained by:** INTELEON404  
**Version:** 3.9 (2025)  
**GitHub:** https://github.com/INTELEON404/RevLookup

---

### Why RevLookup v3.9 Crushes Everything Else

| Feature                          | RevLookup v3.9                          | Others                     |
|----------------------------------|------------------------------------------|----------------------------|
| Speed                            | Up to **5000 threads**                   | Usually < 500             |
| Output                           | **Only hostnames** – no garbage          | Verbose logs & IPs        |
| Input flexibility                | IPs, domains, CIDRs, files (mixed)       | Limited formats           |
| Deduplication                    | Instant `-u` flag                        | Manual post-processing    |
| Single binary / No dependencies  | Yes (pure Python + standard lib)         | Often requires install    |

---

### Features

- ⚡ Lightning-fast multi-threaded reverse DNS (up to **5000 threads**)
- Accepts **IPs**, **domains**, or **entire CIDR ranges**
- Load targets from file (mix IPs, domains, CIDRs freely)
- `-u` → instantly remove duplicate hostnames
- `-td N` → control threads (default: 1000)
- `-o` → save results to file
- **Pure output** – nothing but resolved hostnames
- Gorgeous ASCII banner (disable with `--silent` if needed)

---

### Installation (Zero Dependencies)

#### Option 1 – Clone repository
```bash
git clone https://github.com/INTELEON404/RevLookup.git
cd RevLookup
chmod +x revlookup
sudo mv revlookup /usr/bin
```

#### Option 2 – One-liner (recommended)
```bash
wget https://raw.githubusercontent.com/INTELEON404/RevLookup/main/revlookup -O revlookup
chmod +x revlookup
```

Works on any Linux/macOS with Python 3.6+

---

### Usage Examples


#### Single target (IP or domain)
```
./revlookup -t google.com
./revlookup -t 140.82.113.31
```

# Full CIDR range
```
./revlookup -c 1.1.1.0/24
```

#### From file (IPs, domains, CIDRs – all mixed)
```
./revlookup -f targets.txt
```

#### Pro mode: unique + max threads + save
```
./revlookup -f targets.txt -u -td 4000 -o hosts.txt
```

#### No banner (stealth)
```
./revlookup -t 8.8.8.8 --silent
```

---

### Full Help Menu

```bash
./revlookup -h
```

```
usage: revlookup (-t TARGET | -f FILE | -c CIDR) [-o OUTPUT] [-u] [-td N] [--silent] [-h]

RevLookup v3.9 — Pure Results Only

options:
  -t, --target TARGET      Single IP or domain
  -f, --file FILE          File with targets (one per line)
  -c, --cidr CIDR          CIDR range (e.g. 192.168.1.0/24)
  -o, --output OUTPUT      Save results to file
  -u, --unique             Show only unique hostnames
  -td, --threads N         Max threads (default: 1000, max: 5000)
  --silent                 Hide banner
  -h, --help               Show this help message
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
