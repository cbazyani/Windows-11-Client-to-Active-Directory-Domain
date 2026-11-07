# Windows-11-Client-to-Active-Directory-Domain
This tasks will configure an isolated Windows Server 2025 Active Directory environment and securely join a Windows 11 Pro client machine using VMware Workstation.

<h1>1. Set up Static IP and DNS on Domain Controller</h1>

Best Practice: Servers provide foundational resources that the entire network relies upon to function. Setting a static IP address ensures the server always stays at the exact same network address, preventing it from changing unexpectedly. If you use DHCP for a server, its IP address could change whenever the lease expires or the machine reboots. If the address changes, the network breaks. 

To the find the static IP address to use, open CMD and run the command: ipconfig. I will use the IP address that was assigned to my VM when it was created. 

<img width="599" height="231" alt="image" src="https://github.com/user-attachments/assets/d8f403c5-d617-4d6a-a655-b07cc9b699d0" />

Go to Settings > Network & internet > Ethernet

Under IP assignment, it displays Automatic (DHCP). Click Edit to assign the static IP address to the server.

<img width="1015" height="407" alt="image" src="https://github.com/user-attachments/assets/1b45b10e-3ab3-448e-8b7a-ee6b5984adee" />

Copy the IP address, subnet mask and default gateway to the apparent fields in the Edit IP settings window.

Note: DNS is important because this is how we will join our Windows Client later to the domain. Both the client and the server should be on the same network. The preferred DNS is already filled being the loopback address. The loopback address simply means "look at yourself". Because the Windows Server is the DNS server hosting the Active Directory database, it needs to query its own local DNS service to resolve domain traffic.
