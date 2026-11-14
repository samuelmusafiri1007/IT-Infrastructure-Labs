\# FortiGate Lab: DHCP Server and NAT (EVE-NG)



\## Purpose

Practice configuring a FortiGate firewall as the DHCP server, gateway and NAT device for an isolated lab network.



Cloud (home network) → FortiGate → Cisco switch → Windows client



\## What I Did

* \- Set port1 as the WAN, a DHCP client getting its IP and default gateway from my home router
* \- Set port2 as the LAN with static IP `10.0.10.1/24`
* \- Enabled a DHCP server on port2 (`10.0.10.2` to `10.0.10.254`, gateway and DNS from the FortiGate)
* \- Created a `LAN-to-WAN` firewall policy (port2 to port1) with NAT enabled, this allows the clients to access the internet, FortiGate firewall has a default policy that denies all traffic
* \- Changed adapter settings of the windows clients to receive IPs and DNS config automatically 
* \- Verified the Windows client received its IP, gateway and DNS via DHCP and could reach the internet



