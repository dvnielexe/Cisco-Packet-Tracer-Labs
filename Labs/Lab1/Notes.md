# 📘 Notes — VLAN Segmentation Lab

## 🧠 What is a VLAN?

A VLAN (Virtual Local Area Network) is a logical segmentation of a network that separates devices into different broadcast domains, even if they are connected to the same physical switch.

### 🔹 Key Idea:

Devices in different VLANs **cannot communicate directly** without a Layer 3 device (router or Layer 3 switch).

---

## 🧩 Why VLANs Matter

* Improve **security** (isolate departments)
* Reduce **broadcast traffic**
* Improve **network performance**
* Enable **better organization**

---

## 🔁 Access vs Trunk Ports

### Access Port

* Belongs to a single VLAN
* Used for end devices (PCs)

```
switchport mode access
switchport access vlan 10
```

---

### Trunk Port

* Carries multiple VLANs
* Used between switches or switch → router

```
switchport mode trunk
```

Uses **802.1Q tagging** to identify VLAN traffic.

---

## 🌐 Router-on-a-Stick (ROAS)

A method of enabling inter-VLAN communication using:

* One physical router interface
* Multiple subinterfaces (one per VLAN)

Example:

```
interface g0/0.10
encapsulation dot1Q 10
ip address 192.168.10.1 255.255.255.0
```

---

## 🔐 Security Notes

* VLANs reduce lateral movement in attacks
* Sensitive departments (e.g., Finance) should be isolated
* Use ACLs to control inter-VLAN access

Example:

```
access-list 100 deny ip 192.168.10.0 0.0.0.255 192.168.20.0 0.0.0.255
access-list 100 permit ip any any
```

---

## 🚨 Common Issues & Troubleshooting

### 1. VLAN Not Working

Check:

```
show vlan brief
```

---

### 2. No Inter-VLAN Communication

Check:

* Router subinterfaces configured correctly
* Correct VLAN IDs
* Default gateway on PCs

---

### 3. Trunk Issues

Check:

```
show interfaces trunk
```

---

### 4. Interface Down

Fix:

```
no shutdown
```

---

### 5. Wrong IP Addressing

Ensure:

* Correct subnet
* Correct gateway

---

## 🧪 Useful Commands

| Command                 | Purpose                 |
| ----------------------- | ----------------------- |
| show vlan brief         | View VLANs              |
| show interfaces trunk   | Verify trunk            |
| show ip interface brief | Check router interfaces |
| ping                    | Test connectivity       |

---

## 🧠 Key Takeaways

* VLAN = logical separation
* Trunk = carries multiple VLANs
* Router = enables communication
* Segmentation = security + performance
