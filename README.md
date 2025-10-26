# 🔥 Task 4: Setup and Use a Firewall on Windows/Linux

## 🎯 Objective
Configure and test basic firewall rules to allow or block network traffic.

---

## 🧰 Tools Used
- **Linux:** UFW (Uncomplicated Firewall)
- **Windows:** Windows Defender Firewall

---

## 🧩 Steps Performed

### 🐧 Linux (UFW)
1. Check UFW status and enable if inactive:
   
   sudo ufw status
   sudo ufw enable
   
2. List current rules:
   
   sudo ufw status numbered
   
3. Block inbound traffic on port 23 (Telnet):
   
   sudo ufw deny 23
   
4. Test connection:
   
   telnet localhost 23
   
   (It should say *connection refused* if blocked)
5. Allow SSH (port 22):
   
   sudo ufw allow 22
   
6. Remove test block rule:
   
   sudo ufw delete deny 23
   
7. Show active rules (for screenshot):
   
   sudo ufw status verbose
   

---

### 🪟 Windows Firewall
1. Open Firewall Settings:
   - Press `Win + R`, type `wf.msc`, and press Enter.
2. Go to **Inbound Rules → New Rule**.
3. Choose **Port → TCP → 23 → Block the connection**.
4. Test:
   
   telnet localhost 23
   
   (It should say *Could not open connection*)
5. Add another rule for port **22 → Allow the connection**.
6. Delete the Telnet block rule after testing.

---

## 📸 Screenshots
- `linux/screenshot.png` → Shows UFW rules.
- `windows/screenshot.png` → Shows Windows inbound rules.

---

## 🧠 Summary
A firewall filters traffic by allowing or denying packets based on rules.  
- **Allow rules:** permit specific connections (e.g., SSH on port 22).  
- **Deny rules:** block unwanted connections (e.g., Telnet on port 23).  

This demonstrates how firewalls control access and secure systems from unauthorized traffic.

---

## 👤 Author
**Sumit Kumar Ram**  
BCA 3rd Year, ABS Academy of Science, Technology & Management  
Cybersecurity Enthusiast ⚡
