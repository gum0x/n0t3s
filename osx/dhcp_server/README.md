# Quick dns server to provide IP to a device connected by Ethernet to our Mac

This is useful in order to give IP to raspberry or to a PC directly connecter to our mac

## Dependencies

* dnsmasq

## Howto

```bash
# Enabling IP forwarding
sudo sysctl -w net.inet.ip.forwarding=1

# Connect the ethernet cable and configure the IP
sudo ifconfig en3 add 192.168.2.254/24

# Enabling masquerade 
sudo pfctl -f pfctl.conf -e

# start the dnsmasq process
sudo dnsmasq -C dnsmasq.conf -k -8 -
```

