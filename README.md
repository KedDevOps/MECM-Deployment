# MECM-Deployment  
🚀 **Deploying MECM Using Three Windows Server VMs in Azure**

## 📘 Overview  
This project demonstrates how to deploy **Microsoft Endpoint Configuration Manager (MECM)** in a cloud-based lab environment using three Windows Server virtual machines (VMs) hosted on **Microsoft Azure**. The deployment is designed to replicate an enterprise architecture for **testing, demonstration, and training purposes**.

---

## 🧱 Architecture  

### Core Infrastructure (Azure East - AZE)

| VM Name         | Role                 | Purpose                                      |
|----------------|----------------------|----------------------------------------------|
| AZE-DC01        | Domain Controller    | Hosts Active Directory, DNS, and DHCP        |
| AZE-SQL01       | SQL Server           | Hosts the MECM site database                 |
| AZE-MECM-PS01   | MECM Primary Site    | Installs and runs Microsoft Endpoint Manager |

### Client Devices

| VM Name         | Location      | Purpose                            |
|----------------|---------------|------------------------------------|
| AZE-Device01    | Azure East    | Simulates a managed client device  |
| AZC-Device02    | Azure Central | Simulates a managed client device  |

---

## 🌐 Networking Layout  

| Component               | East US (AZE)   | Central US (AZC)   |
|------------------------|-----------------|--------------------|
| Virtual Network (VNet) | AZE-vnet-01     | AZC-vnet-02        |
| NSG                    | AZE-NSG-01      | AZC-NSG-02         |
| VNet Peering           | ↔ Bi-directional between AZE and AZC |

- Virtual networks are peered to allow secure cross-region communication.
- NSGs are configured per region to control and secure traffic.
- All resources are deployed in the `MECM-Deployment` **Resource Group**.





