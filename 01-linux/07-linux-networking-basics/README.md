
# 🌐 Linux Networking Basics 

Networking is one of the most **important skills** in DevOps.  
You’ll constantly deal with servers, containers, cloud VMs - all of which need **network connectivity** to work together.  

Let’s get practical with Linux networking commands 👇



## 🖧 Check Your IP & Network Info

### 🏠 `ip addr` – Show IP Addresses
```bash
ip addr
````

Shows all network interfaces and their IPs.

Old but still used:

```bash
ifconfig
```

(Install with `sudo apt install net-tools` if missing)



### 🌍 `hostname` – Show Hostname

```bash
hostname
hostname -I   # Show IP address only
```



### 🧭 `ip route` – Show Routing Table

```bash
ip route
```

Shows default gateway and routes.



## 📡 Connectivity Tests

### 📍 `ping` – Check Connectivity

```bash
ping google.com
ping -c 4 google.com   # Send only 4 packets
```



### 🔌 `curl` – Check Web Response

```bash
curl google.com
curl -I google.com  # Show only headers (good for HTTP status check)
```



### 🔎 `nslookup` – DNS Lookup

```bash
nslookup google.com
```

Shows IP address of a domain name.



### 🧩 `dig` – Detailed DNS Lookup

```bash
dig google.com
```

(Install: `sudo apt install dnsutils`)



### 🛠 `traceroute` – Trace Route to Host

```bash
traceroute google.com
```

Shows path your packets take to reach destination.



## 👀 Monitor Active Connections

### 🔗 `netstat` – Network Statistics

```bash
netstat -tulnp
```

* `t` = TCP
* `u` = UDP
* `l` = Listening
* `n` = Show numbers instead of names
* `p` = Show process using port

Install if missing:

```bash
sudo apt install net-tools
```



### 🧠 `ss` – Socket Statistics (Better `netstat`)

```bash
ss -tuln
```

Lists listening ports with protocol.



### 📡 `arp` – Show ARP Table

```bash
arp -n
```

Shows IP → MAC address mapping.



## 🔗 Network Configuration

### 📴 Bring Interface Down / Up

```bash
sudo ip link set eth0 down
sudo ip link set eth0 up
```



### 🆕 Assign New IP (Temporarily)

```bash
sudo ip addr add 192.168.1.50/24 dev eth0
```



## 📊 Bandwidth & Performance

### 📶 `iftop` – Real-Time Bandwidth Usage

```bash
sudo apt install iftop -y
sudo iftop
```



### ⚡ `iperf3` – Test Network Speed

```bash
iperf3 -s   # On one machine (server)
iperf3 -c <server-ip>  # On another machine (client)
```



## 📝 Summary Checklist

✅ Check IP & hostname with `ip addr`, `hostname`
✅ Test connectivity with `ping`, `curl`, `nslookup`, `dig`
✅ Trace routes with `traceroute`
✅ Monitor active connections with `netstat`, `ss`
✅ Configure network interface with `ip link` and `ip addr`
✅ Measure bandwidth with `iftop`, `iperf3`



⚡ **Pro Tip:** Always test connectivity step by step:
1️⃣ Check your IP → 2️⃣ Ping gateway → 3️⃣ Ping external site → 4️⃣ Curl website → 5️⃣ Check routes if something fails.



This module will make you **confident in troubleshooting network issues** on any Linux server - a must-have skill for DevOps.

