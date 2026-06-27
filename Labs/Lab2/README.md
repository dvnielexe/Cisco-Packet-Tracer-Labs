# 🔐 Network Access Control Using ACLs (Cisco Packet Tracer Lab)

## 📖 Scenario

A company network consists of three departments:

* Human Resources (HR)
* Finance
* IT

Each department is placed on its own subnet and connected through a central router.

Due to internal security policies:

* ❌ HR must NOT access the Finance network
* ❌ Finance must NOT access the HR network
* ✅ IT must have full access to both HR and Finance networks
* ✅ All departments should still be able to communicate with their default gateway

As a network engineer, your task is to configure **Access Control Lists (ACLs)** to enforce these restrictions.

---

## 🎯 Objectives

* Understand how Access Control Lists (ACLs) work
* Configure Extended ACLs on a router
* Apply ACLs to interfaces correctly
* Verify traffic filtering using connectivity tests

---

## 🏗️ Network Design

| Department | Network         | Example Host  |
| ---------- | --------------- | ------------- |
| HR         | 192.168.10.0/24 | 192.168.10.10 |
| Finance    | 192.168.20.0/24 | 192.168.20.10 |
| IT         | 192.168.30.0/24 | 192.168.30.10 |

---

## ⚙️ Key Configuration Summary

* Router configured with 3 interfaces (one per network)
* Extended ACL used to filter traffic between HR and Finance
* ACL applied **inbound** on relevant interfaces

---

## 🧪 Testing & Verification

### Expected Results:

| Source        | Destination | Result |
| ------------- | ----------- | ------ |
| HR → Finance  | ❌ Blocked   |        |
| Finance → HR  | ❌ Blocked   |        |
| IT → HR       | ✅ Allowed   |        |
| IT → Finance  | ✅ Allowed   |        |
| All → Gateway | ✅ Allowed   |        |

---

## 🧠 What This Lab Demonstrates

* Real-world network segmentation
* Basic internal security enforcement
* Proper ACL placement and logic
* Troubleshooting access issues

---

## 🚀 Author

Created as part of hands-on networking and cybersecurity practice using Cisco Packet Tracer.
