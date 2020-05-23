
# Information Gathering

## Whois Lookups
* Displays information about the owner.
* whois bulbsecurity.com

## DNS Reconnaissance
**Nslookup**
* Returns the IP of an address, can also find mail servers for a site.
* nslookup
* > set type=mx
* > bulbsecurity.com

## Host
* Also performs DNS queries
* host -t ns zoneedit.com
* Output will show all the DNS servers for zoneedit.com

## Zone Transfers
* DNS zone transfers allow name servers to replicate all the entries about a domain.
* host -l zoneedit.com ns2.zoneedit.com

## Syn Scan
* A SYN scan is a TCP scan that does not finish the TCP handshake. 
* nmap sends the SYN and waits for the SYN-ACK if the port is open but never sends the ACK to complete the connection.
* If the SYN packet receives no SYN-ACK response, the port is either closed or filtered. This way, nmap finds out if a
port is open without ever fully connecting to the target machine.
* -sS is the flag for a SYN scan.
* -oA will output in all file formats. This includes a greppable format to search for specific information
