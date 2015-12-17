PowerDNS Authoritative server and Poweradmin
===========
# Quickstart

```wget https://raw.githubusercontent.com/obi12341/docker-pdns/master/docker-compose.yml && docker-compose up -d```

# Running

Just use this command to start the container. PowerDNS will listen on port 53/tcp, 53/udp and 8080/tcp.

```docker run --name pdns-master -e MYSQL_HOST='aHOST' -e MYSQL_DB='aDB' -e MYSQL_USER='aUSER' -e MYSQL_PASSWORD='aPASSWORD'-d -p 53:53/udp -p 53:53 -p 8080:80 secns/pdns```

# Configuration
These options can be set:

- **PDNS_ALLOW_AXFR_IPS**: restrict zonetransfers to originate from these IP addresses. Enter your slave IPs here. (Default: "127.0.0.1", Possible Values: "IPs comma seperated")
- **PDNS_MASTER**: act as master (Default: "yes", Possible Values: "yes, no")
- **PDNS_SLAVE**: act as slave (Default: "no", Possible Values: "yes, no")
- **POWERADMIN_HOSTMASTER**: default hostmaster (Default: "", Possible Values: "<email>")
- **POWERADMIN_NS1**: default Nameserver 1 (Default: "", Possible Values: "<domain>")
- **POWERADMIN_NS2**: default Nameserver 2 (Default: "", Possible Values: "<domain>")
