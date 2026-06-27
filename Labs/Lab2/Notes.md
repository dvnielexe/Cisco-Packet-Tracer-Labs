# 🧠 Access Control Lists (ACLs) — Notes

## 📌 What is an ACL?

An **Access Control List (ACL)** is a set of rules used on routers and switches to control network traffic.

ACLs determine whether to **permit or deny packets** based on defined conditions such as IP address, protocol, or port number.

---

## 🎯 Purpose of ACLs

ACLs are used to:

* Restrict unauthorized access between networks
* Enforce security policies
* Control traffic flow
* Reduce unnecessary network traffic
* Segment internal networks

---

## 🔍 Types of ACLs

### 1. Standard ACL

* Filters traffic based on **source IP address only**
* Simpler but less flexible

Example:
permit 192.168.10.0 0.0.0.255

---

### 2. Extended ACL

* Filters based on:

  * Source IP
  * Destination IP
  * Protocol (TCP, UDP, ICMP)
  * Port numbers

* Provides **more precise control**

Example:
deny ip 192.168.10.0 0.0.0.255 192.168.20.0 0.0.0.255

---

## ⚙️ How ACLs Work

* ACLs are processed **top-down**
* The first matching rule is applied
* Every ACL ends with an **implicit deny**:

  deny ip any any

This means anything not explicitly allowed is automatically blocked.

---

## 📍 ACL Placement Rules

* **Standard ACLs** → Place close to destination
* **Extended ACLs** → Place close to source

This helps reduce unnecessary traffic across the network.

---

## 🔢 Wildcard Masks Explained

Wildcard masks are used in ACLs to define ranges of IP addresses.

Example:

0.0.0.255 = match all hosts in a /24 network

It works as the inverse of a subnet mask.

---

## 🧪 Common Mistakes

* Applying ACL in the wrong direction (in/out)
* Incorrect wildcard mask
* Forgetting `permit ip any any`
* Misordering rules (order matters!)
* Not enabling interfaces (`no shutdown`)

---

## 🛠️ Useful Commands

Check ACL:
show access-lists

Check interface ACL application:
show ip interface

---

## 🧩 Summary

ACLs are a fundamental network security tool that allow administrators to control who can access what within a network.

In real-world environments, ACLs are used alongside firewalls and other security systems to enforce strict access policies.
