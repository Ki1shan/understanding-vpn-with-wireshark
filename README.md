# 🛡️ Working and Understanding VPN

## 🎯 Objective
To understand how Virtual Private Networks (VPNs) protect online privacy and secure communications by masking IP addresses and encrypting internet traffic. This project includes setup, real-world testing, and packet inspection using Wireshark.

---

## 🧰 Tools Used

- ✅ [ProtonVPN (Free Tier)](https://protonvpn.com)
- ✅ [Wireshark](https://www.wireshark.org/)
- ✅ [whatismyipaddress.com](https://www.whatismyipaddress.com)
- ✅ [Cybrary](https://www.cybrary.it)
- ✅ [Speedtest by Ookla](https://www.speedtest.net)
- ✅ Kali Linux (Oracle VirtualBox)
- ✅ Terminal-based VPN commands (ProtonVPN CLI)

---

## 🔧 Steps Performed

1. **Signed up** for ProtonVPN (Free Tier).
2. **Installed** ProtonVPN CLI on Kali Linux.
3. **Connected** to the fastest VPN server using:
   ```
   protonvpn init
   protonvpn connect --fastest
   ```
4. **Verified IP change** using [whatismyipaddress.com](https://www.whatismyipaddress.com).
5. **Tested internet speed** before and after VPN using [Speedtest.net](https://www.speedtest.net).
6. **Browsed encrypted websites** like whatismyipaddress.com and cybrary.it while connected.
7. **Used Wireshark** to inspect packet traffic before and after connecting to the VPN:
   - **Interface before VPN**: `eth0`
   - **Interface after VPN**: `tun0`
   - **Applied filters**:
     - To check visible IPs: `ip.addr == YOUR_IP_ADDRESS`
     - To inspect encrypted traffic: `tls`
8. **Compared packet data** before vs. after VPN to confirm encryption and tunneling.

---

## 🧪 Key Findings

- Real IP address was successfully masked after VPN connection.
- Encrypted TLS traffic confirmed via Wireshark capture.
- VPN tunneled traffic securely through `tun0` interface.
- DNS requests were protected (no leaks observed).
- Slight speed drop noted, but performance remained acceptable.

---

## 🔐 Benefits of VPN

- IP masking for privacy protection
- Encrypted communication on public networks
- Bypassing geo-restrictions
- Protection from ISP surveillance and MITM attacks

---

## ⚠️ Limitations Observed

- Slight reduction in internet speed after VPN connection
- Free-tier VPNs may have limited server options
- Some websites may block known VPN IPs

