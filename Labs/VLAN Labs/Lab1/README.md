## 🏢 Small Office Network Segmentation Using VLANs

## 📖 Scenario

A growing company has multiple departments:

* HR
* Finance
* IT

Currently, all devices are on the same flat network, leading to:

* Security risks (unauthorized access to sensitive systems)
* Broadcast congestion
* Poor network organization

As a network engineer, your task is to redesign the network using VLANs to improve security, performance, and scalability.

---

## 🎯 Objectives

* Create VLANs for each department
* Assign switch ports to appropriate VLANs
* Configure trunk links
* Enable inter-VLAN communication using Router-on-a-Stick
* Test and verify connectivity

---

## 🖧 Topology

* 1 Router
* 1 Switch
* 6 PCs (2 per department)

| Department | VLAN | Network         |
| ---------- | ---- | --------------- |
| HR         | 10   | 192.168.10.0/24 |
| Finance    | 20   | 192.168.20.0/24 |
| IT         | 30   | 192.168.30.0/24 |

---

## ⚙️ Key Features Implemented

* VLAN segmentation
* Access port configuration
* 802.1Q trunking
* Router-on-a-Stick (Inter-VLAN routing)
* Network testing and verification

---

## 🧪 Testing

| Test                     | Expected Result            |
| ------------------------ | -------------------------- |
| Same VLAN communication  | ✅ Success                  |
| Inter-VLAN communication | ✅ Success via router       |
| VLAN verification        | ✅ Correct VLAN assignments |

---

## 🔐 Security Insight

Network segmentation reduces the attack surface. If one VLAN is compromised, attackers cannot easily access other departments.

---

## 🚀 Real-World Relevance

This setup is commonly used in:

* Corporate offices
* Banks
* Universities
* Enterprise networks

---

## 📁 Project Structure

```
network-segmentation-vlan-lab/
│
├── README.md
├── Notes.md
├── configs.txt
└── packet_tracer/
    └── vlan_lab.pkt
```

---

## 💡 What I Learned

* How VLANs isolate broadcast domains
* How trunking allows multiple VLANs on one link
* How routers enable communication between VLANs
* Basic network segmentation for security

---

## 🏁 Conclusion

This lab demonstrates a foundational network security concept—segmentation using VLANs—and shows how proper configuration improves both performance and security in real-world environments.
