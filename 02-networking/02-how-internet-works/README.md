
# 02 - How the Internet Works

Welcome to **Module 2: How the Internet Works**! 🌐  
In this module, we’ll go **deeper into the workings of the internet**, with real-world examples and practical insights that DevOps engineers use daily.  



## 📌 What is the Internet?

- The **Internet** is a **global network of computers** connected together to **share information and resources**.  
- Think of it like a **giant postal system**: every message (data) is delivered from one computer to another through multiple paths.  
- Every device on the internet has an **IP address** (like a home address) to receive data correctly.  

**Real-world example:**  
- You send a video on WhatsApp → your device splits it into **small packets** → packets travel across networks → reach your friend's device → packets are reassembled → your friend sees the video.  



## 🏷 Client-Server Model

- **Client**: Your device (computer, phone, laptop) that **requests data**.  
- **Server**: A device that **provides data** (websites, APIs, databases).  
- Communication is usually **request-response**.  

**Example:**  
1. Open `https://www.google.com` on your browser → **Client sends HTTP request** to Google server.  
2. Google server processes request → **Server sends response** (HTML, CSS, JS files).  
3. Browser renders the page → you see Google homepage.  

**Hands-on Example:**  
```bash
curl -I https://www.google.com   # Shows HTTP headers returned by server
ping google.com                  # Checks connectivity to server
traceroute google.com            # Shows path taken by packets to reach server
````


## 📡 How Data Travels: Packets & Routing

* Data is never sent as a **single large file**. It’s split into **packets**.

* Each packet contains:

  * Source IP
  * Destination IP
  * Sequence number (to reassemble correctly)
  * Payload (actual data)

* Packets travel through **routers**, which forward them toward the destination based on routing tables.

**Real-world example:**

* Sending an email → Email server splits email into packets → Packets go through ISP routers → Reach recipient server → Email client reassembles email → Recipient reads it.

**Commands to inspect:**

```bash
ping google.com           # Tests packet delivery
traceroute google.com     # Shows path packets take
mtr google.com            # Combines ping & traceroute for live tracking
```


## ⚡ Summary

* Internet = Global network of connected computers
* Uses **Client-Server Model** for communication
* Data is split into **packets** and routed via **routers**
* Practically, you can **ping, traceroute, curl, nslookup** to test connectivity


💡 **Pro Tip:** Open your browser dev tools → Network tab → Watch requests when loading a webpage. Each line = a real-life packet traveling across the internet!

