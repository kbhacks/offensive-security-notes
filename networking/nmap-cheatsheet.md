#nmap essentials.

nmap 
- network mapper
- A great tool to figure out what(hosts) you have in your surroundings and what do they have in them.

- `nmap <target-ip>` : performs a TCP connect scan
- `sudo nmap <target-ip>` : performs a TCP SYN scan
-- Note: If you provide a domain like, google.com, nmap will first convert it to a IP and then perform the scan.

Switches => These are great to tweak the scan.
-sT --- 1. TCP connect scan
	2. Performs a 3-way handshake with the target, SYN SYN/ACK ACK
	3. If the target is accepting connection on that port, that is the port is OPEN, the target(e.g, server) will respond with a TCP packet with ACK set as 1.
	4. If the target port is CLOSED, TCP packet with RST (RESET) set is 1 is sent as response to the TCP packet with SYN set as 1 from your machine.
	5. If the target is behind firewall, and the firewall is dropping the input SYN TCP packet, you will get the port marked as FILTERED.
	6. The firewall can also be configured to respond with a RST rather than just dropping, for example, with linux iptables : 

-sS --- 1. SYN scan/ half-open scan/ Stealth scan
	2.  	
