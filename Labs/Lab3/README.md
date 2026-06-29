# 🏠 Home Network Simulation (Cisco Packet Tracer)

## 📖 Scenario

You are setting up a small home network with both wired and wireless devices.

The network consists of:

* A wireless router (acts as gateway, DHCP server, and access point)
* A switch for wired connections
* Two wired PCs
* One laptop and one smartphone connected via WiFi

The router connects to an ISP using a public IP address and provides private IP addresses to internal devices using DHCP.

---

## 🎯 Objectives

* Configure a wireless router with:

  * WAN (ISP) settings
  * LAN gateway
  * DHCP services
  * Wireless access (SSID + security)
* Connect wired devices through a switch
* Connect wireless devices via WiFi
* Verify full connectivity across all devices

---

## 🌐 Network Details

| Component     | Configuration               |
| ------------- | --------------------------- |
| WAN IP        | 203.0.113.2/30              |
| Gateway (ISP) | 203.0.113.1                 |
| LAN Network   | 192.168.1.0/24              |
| Router LAN IP | 192.168.1.1                 |
| DHCP Range    | 192.168.1.10 – 192.168.1.50 |
| DNS Server    | 8.8.8.8                     |
| SSID          | HomeWiFi                    |
| WiFi Password | home12345                   |

---

## 🧪 Verification Tests

* All devices receive IP via DHCP
* Devices can ping:

  * Router (192.168.1.1)
  * Each other
* Wireless devices can communicate with wired devices

---

## 🧠 Skills Learned

* DHCP configuration
* Basic home network design
* Wireless security setup
* LAN switching
* End-to-end connectivity testing

---
