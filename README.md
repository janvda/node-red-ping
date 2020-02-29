ping
====

This flows measures every 5 sec the ping times of several hosts and shows it in charts in the ping tab of the node-red UI dashboard.

Moreover the ping times are also stored in an influx database which can be visualized in a graphana dashboard.

## screenshot of the node-red dashboard

![screenshot node-red dashboard](screenshot_node_red_dashboard.png)

## a screenshot example of a graphana dashboard

![screenshot graphana dashboard](screenshot_graphana_dashboard.png)

# prerequisites
1. Requires an influx database with following specs:
 - server:port = influxdb:8086
 - database = ping
 - no username and password
 - it is adviced to set the retention policy less than 1 week

# Notes
 1. macOS’s firewall can block the ICMP packets that ping uses, which will interfere with this test. Make sure you disable “Stealth Mode” in “System Preferences”->“Security & Privacy” -> “Firewall
 2. Currently my macbook doesn't get the same IP address from DHCP - so you might need to manually update the flow for this.