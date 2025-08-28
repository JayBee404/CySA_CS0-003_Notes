Some simple tcpdump commands:

- `sudo tcpdump -i [eth|en]0` - basic listening for all traffic
- `sudo tcpdump src x.x.x.x` - listens for all traffic from a specific source
- `sudo tcpdump src x.x.x.x -w file_name.pcap` - same as above but writes data to file
- `sudo tcpdump -r file_name.pcap` - read and display all packets from file
- `sudo tcpdump src port xxxx` - Displays all traffic from a source port
- `sudo tcpdump  -X` - Displays all traffic in hex and ASCII