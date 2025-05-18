# MECM-Deployment
# 🚀 Deploying MECM Using Three Windows Server VMs in Azure

## 📘 Overview

This project demonstrates how to deploy **Microsoft Endpoint Configuration Manager (MECM)** in a cloud-based lab environment using **three Windows Server virtual machines (VMs)** hosted on **Microsoft Azure**. The deployment is designed to replicate an enterprise architecture for testing, demonstration, and training purposes.

---

## 🧱 Architecture

| VM Name  | Role                  | Purpose                                      |
|----------|-----------------------|----------------------------------------------|
| `DC01`   | Domain Controller     | Hosts Active Directory, DNS, and DHCP        |
| `SQL01`  | SQL Server            | Hosts the MECM site database                 |
| `MECM-PS-01` | MECM Primary Site     | Installs and runs Microsoft Endpoint Manager |




