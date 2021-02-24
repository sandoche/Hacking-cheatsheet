# Nmap cheatsheet

```sh
# Discovers IPs
nmap -v -sn 192.168.10.1-254

# Run a TCP Scan on all the ports
# remove -p- to not scan all the ports
nmap -sT -p- -Pn 192.168.10.1-254

# Run a SYN Scan (SYN is the default mode)
nmap -sS -p- -Pn 192.168.10.1-254

# Run a UDP Scan, replace -sT with -sU
# -p- and -Pn has been removed because UDP scans are very slow
nmap -sUV 192.168.10.1-254

# Run a XMAS Scan
nmap -sX -p- -Pn 192.168.10.1-254

# Run a NULL Scan
nmap -sN -p- -Pn 192.168.10.1-254

# Replace the range to a specific IP to scan all the ports of one IP

# Nmap script banner
nmap --script banner 192.168.10.11

# Nmap script vuln
nmap --script vuln 192.168.10.11
```