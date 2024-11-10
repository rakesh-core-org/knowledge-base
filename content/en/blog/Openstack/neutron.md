Get mac address 

`getmac /v`
`route print` or `get-netroute`


layer-3 switch --> has routing capability (Inter VLAN Routing)

APIPA --> will comes into picture when no DHCP is configured. IP address will be like 169.254.x.x


# DHCP 

DHCP database --> dhcp.mdb
Default lease duration is 8 days    


DHCP authorization -- exclusive for microsoft windows 
    only authorized DHCP servers can lease IPaddress 


DHCP address exclution

DHCP secondary server: for second server add subnet delay (split scope)
    DHCP failover

DHCP reservation --> based on mac address, IP address can be reserved


# DNS 

zones
    resource records (A, AAA, cname,SRV)
    DNS resolver

SRV- service locator (if we don't know IP address or computer name, our DNS server will give details like who host kerbros authentication)

Zone 
    forward lookup zone (name to IP)
    reverse lookup zone (IP to name) (eg. PTR)


# Openflow 
    its a protocol, not SDN . Its a southbound interfaces. openflow one of the implementation
