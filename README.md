# Windows-11-Client-to-Active-Directory-Domain
This tasks will configure an isolated Windows Server 2025 Active Directory environment and securely join a Windows 11 Pro client machine using VMware Workstation.

<h1>1. Set up Static IP and DNS on Domain Controller</h1>

Best Practice: Servers provide foundational resources that the entire network relies upon to function. Setting a static IP address ensures the server always stays at the exact same network address, preventing it from changing unexpectedly. If you use DHCP (Dynamic Host Configuration Protocol) for a server, its IP address could change whenever the lease expires or the machine reboots. If the address changes, the network breaks.
