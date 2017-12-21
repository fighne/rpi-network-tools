# rpi-nflowd

There are two ways to install and configure the NetFlow process.
* The first way is to use the packets capture by tcpdump can convert them to netflow
* The second way is to directly use the netflow daemon to capture directly.
Personally I prefer the first option as you then have the packets to inspect later, so I'll be covering that first.