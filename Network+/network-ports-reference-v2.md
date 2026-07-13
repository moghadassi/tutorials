# Network Ports Reference

A comprehensive, ordered reference of TCP/UDP network ports — from the well-known range (0–1023) through registered (1024–49151) and commonly used dynamic/private ports — including category and security notes for each.

## Table of Contents

- [Port Ranges Overview](#port-ranges-overview)
- [Well-Known Ports (0–1023)](#well-known-ports-0-1023)
- [Registered Ports (1024–49151)](#registered-ports-1024-49151)
- [Dynamic / Private Ports (49152–65535)](#dynamic--private-ports-49152-65535)
- [Contributing](#contributing)

---

## Port Ranges Overview

| Range | Name | Description |
|-------|------|-------------|
| 0–1023 | Well-Known / System Ports | Assigned by IANA to standard services, require root/admin privileges on most OSes |
| 1024–49151 | Registered Ports | Registered with IANA by software vendors for specific applications |
| 49152–65535 | Dynamic / Private / Ephemeral Ports | Used for temporary/client-side connections, not assigned to specific services |

**Security column legend:**
- 🔴 **Insecure** — plaintext/unencrypted, avoid exposing publicly
- 🟡 **Legacy** — outdated protocol, deprecated or commonly abused
- 🟢 **Secure** — encrypted by default (TLS/SSL/SSH)
- ⚪ **Depends** — security depends on configuration/implementation

---

## Well-Known Ports (0–1023)

| Port | Protocol | Service | Category | Security | Description |
|------|----------|---------|----------|----------|--------------|
| 7 | TCP/UDP | Echo | Diagnostic | 🔴 Insecure | Echo Protocol |
| 9 | TCP/UDP | Discard | Diagnostic | 🔴 Insecure | Discard Protocol |
| 13 | TCP/UDP | Daytime | Diagnostic | 🔴 Insecure | Daytime Protocol |
| 19 | TCP/UDP | Chargen | Diagnostic | 🟡 Legacy | Character Generator (DDoS-abusable) |
| 20 | TCP | FTP-DATA | File Transfer | 🔴 Insecure | FTP Data Transfer |
| 21 | TCP | FTP | File Transfer | 🔴 Insecure | File Transfer Protocol (Control) |
| 22 | TCP | SSH | Remote Access | 🟢 Secure | Secure Shell |
| 23 | TCP | Telnet | Remote Access | 🔴 Insecure | Telnet Protocol (plaintext) |
| 25 | TCP | SMTP | Email | 🔴 Insecure | Simple Mail Transfer Protocol |
| 37 | TCP/UDP | Time | Diagnostic | 🔴 Insecure | Time Protocol |
| 42 | TCP/UDP | WINS | Directory | ⚪ Depends | Host Name Server |
| 43 | TCP | WHOIS | Directory | 🔴 Insecure | WHOIS Protocol |
| 53 | TCP/UDP | DNS | Directory / DNS | ⚪ Depends | Domain Name System |
| 67 | UDP | DHCP-Server | Network Infra | ⚪ Depends | DHCP Server |
| 68 | UDP | DHCP-Client | Network Infra | ⚪ Depends | DHCP Client |
| 69 | UDP | TFTP | File Transfer | 🔴 Insecure | Trivial File Transfer Protocol |
| 79 | TCP | Finger | Diagnostic | 🔴 Insecure | Finger Protocol (info leak) |
| 80 | TCP | HTTP | Web | 🔴 Insecure | Hypertext Transfer Protocol |
| 88 | TCP/UDP | Kerberos | Authentication | 🟢 Secure | Kerberos Authentication |
| 109 | TCP | POP2 | Email | 🔴 Insecure | Post Office Protocol v2 |
| 110 | TCP | POP3 | Email | 🔴 Insecure | Post Office Protocol v3 |
| 111 | TCP/UDP | RPCbind | RPC | 🟡 Legacy | ONC RPC / Portmapper |
| 113 | TCP | Ident | Authentication | ⚪ Depends | Identification Protocol |
| 119 | TCP | NNTP | Messaging | 🔴 Insecure | Network News Transfer Protocol |
| 123 | UDP | NTP | Network Infra | ⚪ Depends | Network Time Protocol (amplification-abusable) |
| 135 | TCP/UDP | MS RPC | RPC | 🔴 Insecure | Microsoft RPC Endpoint Mapper |
| 137 | TCP/UDP | NetBIOS-NS | File Sharing | 🔴 Insecure | NetBIOS Name Service |
| 138 | TCP/UDP | NetBIOS-DGM | File Sharing | 🔴 Insecure | NetBIOS Datagram Service |
| 139 | TCP/UDP | NetBIOS-SSN | File Sharing | 🔴 Insecure | NetBIOS Session Service |
| 143 | TCP | IMAP | Email | 🔴 Insecure | Internet Message Access Protocol |
| 161 | UDP | SNMP | Monitoring | 🟡 Legacy | Simple Network Management Protocol (v1/v2 insecure) |
| 162 | UDP | SNMP-Trap | Monitoring | 🟡 Legacy | SNMP Trap |
| 179 | TCP | BGP | Routing | ⚪ Depends | Border Gateway Protocol |
| 194 | TCP/UDP | IRC | Messaging | 🔴 Insecure | Internet Relay Chat |
| 220 | TCP/UDP | IMAP3 | Email | 🔴 Insecure | Interactive Mail Access Protocol v3 |
| 389 | TCP/UDP | LDAP | Directory | 🔴 Insecure | Lightweight Directory Access Protocol |
| 411 | TCP | Direct Connect | File Sharing | 🔴 Insecure | Direct Connect Hub |
| 427 | TCP/UDP | SLP | Discovery | 🟡 Legacy | Service Location Protocol |
| 443 | TCP | HTTPS | Web | 🟢 Secure | HTTP Secure (TLS/SSL) |
| 445 | TCP | Microsoft-DS | File Sharing | 🟡 Legacy | SMB / Active Directory (major attack vector) |
| 464 | TCP/UDP | Kpasswd | Authentication | 🟢 Secure | Kerberos Change/Set Password |
| 465 | TCP | SMTPS | Email | 🟢 Secure | SMTP over TLS (Submission) |
| 500 | UDP | ISAKMP/IKE | VPN | 🟢 Secure | Internet Key Exchange (IPsec) |
| 512 | TCP | Exec | Remote Access | 🔴 Insecure | Remote Process Execution |
| 513 | TCP | Login | Remote Access | 🔴 Insecure | Remote Login (rlogin) |
| 514 | TCP | Shell | Remote Access | 🔴 Insecure | Remote Command (rsh) |
| 514 | UDP | Syslog | Monitoring | 🔴 Insecure | System Logging Protocol |
| 515 | TCP | LPD | Printing | 🔴 Insecure | Line Printer Daemon |
| 520 | UDP | RIP | Routing | 🟡 Legacy | Routing Information Protocol |
| 523 | TCP/UDP | IBM-DB2 | Database | ⚪ Depends | IBM DB2 |
| 524 | TCP/UDP | NCP | File Sharing | 🟡 Legacy | NetWare Core Protocol |
| 530 | TCP/UDP | RPC | RPC | 🟡 Legacy | Courier RPC |
| 543 | TCP | Klogin | Remote Access | 🟡 Legacy | Kerberos Login |
| 544 | TCP | Kshell | Remote Access | 🟢 Secure | Kerberos Remote Shell |
| 546 | TCP/UDP | DHCPv6-Client | Network Infra | ⚪ Depends | DHCP for IPv6 Client |
| 547 | TCP/UDP | DHCPv6-Server | Network Infra | ⚪ Depends | DHCP for IPv6 Server |
| 548 | TCP | AFP | File Sharing | ⚪ Depends | Apple Filing Protocol |
| 554 | TCP/UDP | RTSP | Streaming | ⚪ Depends | Real Time Streaming Protocol |
| 587 | TCP | SMTP Submission | Email | 🟢 Secure | Email Message Submission (STARTTLS) |
| 593 | TCP/UDP | HTTP-RPC-EPMAP | RPC | 🔴 Insecure | HTTP RPC Endpoint Mapper |
| 623 | UDP | IPMI | Remote Management | 🔴 Insecure | Intelligent Platform Management Interface (widely abused) |
| 631 | TCP/UDP | IPP | Printing | ⚪ Depends | Internet Printing Protocol / CUPS |
| 636 | TCP/UDP | LDAPS | Directory | 🟢 Secure | LDAP over TLS/SSL |
| 646 | TCP/UDP | LDP | Routing | ⚪ Depends | Label Distribution Protocol (MPLS) |
| 691 | TCP | MS-Exchange | Email | ⚪ Depends | MS Exchange Routing |
| 860 | TCP | iSCSI | Storage | ⚪ Depends | iSCSI Protocol |
| 873 | TCP | Rsync | File Transfer | 🔴 Insecure | Remote Sync Protocol (unless tunneled) |
| 902 | TCP/UDP | VMware-Auth | Virtualization | ⚪ Depends | VMware Server Authentication |
| 989 | TCP | FTPS-Data | File Transfer | 🟢 Secure | FTP over TLS (Data) |
| 990 | TCP | FTPS | File Transfer | 🟢 Secure | FTP over TLS (Control) |
| 992 | TCP/UDP | Telnets | Remote Access | 🟢 Secure | Telnet over TLS/SSL |
| 993 | TCP | IMAPS | Email | 🟢 Secure | IMAP over TLS/SSL |
| 995 | TCP | POP3S | Email | 🟢 Secure | POP3 over TLS/SSL |

---

## Registered Ports (1024–49151)

| Port | Protocol | Service | Category | Security | Description |
|------|----------|---------|----------|----------|--------------|
| 1080 | TCP | SOCKS | Proxy | ⚪ Depends | SOCKS Proxy |
| 1099 | TCP | RMI Registry | RPC | 🔴 Insecure | Java RMI Registry (common exploit target) |
| 1194 | TCP/UDP | OpenVPN | VPN | 🟢 Secure | OpenVPN |
| 1241 | TCP/UDP | Nessus | Security Tool | 🟢 Secure | Nessus Vulnerability Scanner |
| 1337 | TCP | WASTE | File Sharing | ⚪ Depends | Encrypted File Sharing |
| 1433 | TCP | MS-SQL | Database | 🔴 Insecure | Microsoft SQL Server (unless TLS enabled) |
| 1434 | UDP | MS-SQL-Monitor | Database | 🔴 Insecure | MS SQL Monitor |
| 1494 | TCP | Citrix ICA | Remote Access | ⚪ Depends | Citrix Independent Computing Architecture |
| 1521 | TCP | Oracle DB | Database | 🔴 Insecure | Oracle Database Listener (unless TLS) |
| 1524 | TCP | Ingreslock | Backdoor | 🔴 Insecure | Common historical backdoor port |
| 1701 | UDP | L2TP | VPN | ⚪ Depends | Layer 2 Tunneling Protocol |
| 1720 | TCP | H.323 | VoIP | ⚪ Depends | H.323 Call Signaling |
| 1723 | TCP | PPTP | VPN | 🟡 Legacy | Point-to-Point Tunneling Protocol (broken crypto) |
| 1812 | UDP | RADIUS | Authentication | ⚪ Depends | RADIUS Authentication |
| 1813 | UDP | RADIUS-Acct | Authentication | ⚪ Depends | RADIUS Accounting |
| 1900 | UDP | SSDP | Discovery | 🔴 Insecure | Simple Service Discovery Protocol (DDoS-abusable) |
| 1935 | TCP | RTMP | Streaming | 🔴 Insecure | Real Time Messaging Protocol |
| 2049 | TCP/UDP | NFS | File Sharing | 🔴 Insecure | Network File System (unless Kerberized) |
| 2082 | TCP | cPanel | Web Hosting Panel | 🔴 Insecure | cPanel Default |
| 2083 | TCP | cPanel-SSL | Web Hosting Panel | 🟢 Secure | cPanel over SSL |
| 2181 | TCP | ZooKeeper | Distributed Systems | 🔴 Insecure | Apache ZooKeeper Client Port |
| 2222 | TCP | SSH-Alt | Remote Access | 🟢 Secure | Alternate SSH / DirectAdmin |
| 2375 | TCP | Docker | Containers | 🔴 Insecure | Docker REST API (unencrypted, critical risk) |
| 2376 | TCP | Docker-TLS | Containers | 🟢 Secure | Docker REST API over TLS |
| 2377 | TCP | Docker Swarm | Containers | 🟢 Secure | Docker Swarm Cluster Management |
| 2379 | TCP | etcd-client | Distributed Systems | ⚪ Depends | etcd Client Communication |
| 2380 | TCP | etcd-peer | Distributed Systems | ⚪ Depends | etcd Peer Communication |
| 3000 | TCP | Dev-Server | Development | 🔴 Insecure | Common Dev Server (Node/Rails/Grafana) |
| 3128 | TCP | Squid Proxy | Proxy | ⚪ Depends | Squid Web Proxy |
| 3260 | TCP | iSCSI-Target | Storage | ⚪ Depends | iSCSI Target |
| 3306 | TCP | MySQL | Database | 🔴 Insecure | MySQL Database (unless TLS enabled) |
| 3389 | TCP | RDP | Remote Access | 🟡 Legacy | Remote Desktop Protocol (frequent ransomware vector) |
| 3690 | TCP | SVN | Version Control | 🔴 Insecure | Subversion Version Control |
| 3724 | TCP/UDP | WoW | Gaming | ⚪ Depends | World of Warcraft |
| 4444 | TCP | Metasploit | Security Tool | 🔴 Insecure | Common Backdoor / Metasploit Default Handler |
| 4500 | UDP | IPsec-NAT-T | VPN | 🟢 Secure | IPsec NAT Traversal |
| 5000 | TCP | UPnP/Flask-Dev | Development | 🔴 Insecure | Universal Plug and Play / Flask Dev Server |
| 5060 | TCP/UDP | SIP | VoIP | 🔴 Insecure | Session Initiation Protocol |
| 5061 | TCP | SIPS | VoIP | 🟢 Secure | SIP over TLS |
| 5222 | TCP | XMPP-Client | Messaging | ⚪ Depends | XMPP / Jabber Client |
| 5223 | TCP | XMPP-SSL | Messaging | 🟢 Secure | XMPP over SSL |
| 5353 | UDP | mDNS | Discovery | ⚪ Depends | Multicast DNS (Bonjour) |
| 5432 | TCP | PostgreSQL | Database | 🔴 Insecure | PostgreSQL Database (unless TLS enabled) |
| 5555 | TCP | ADB | Development | 🔴 Insecure | Android Debug Bridge (frequent malware target) |
| 5601 | TCP | Kibana | Monitoring | ⚪ Depends | Kibana Web Interface |
| 5672 | TCP | AMQP | Messaging | ⚪ Depends | Advanced Message Queuing Protocol (RabbitMQ) |
| 5900 | TCP | VNC | Remote Access | 🔴 Insecure | Virtual Network Computing (weak auth by default) |
| 5938 | TCP | TeamViewer | Remote Access | 🟢 Secure | TeamViewer Remote Access |
| 5984 | TCP | CouchDB | Database | 🔴 Insecure | Apache CouchDB |
| 5985 | TCP | WinRM-HTTP | Remote Management | 🔴 Insecure | Windows Remote Management |
| 5986 | TCP | WinRM-HTTPS | Remote Management | 🟢 Secure | Windows Remote Management over TLS |
| 6000 | TCP | X11 | Remote Access | 🔴 Insecure | X Window System |
| 6379 | TCP | Redis | Database | 🔴 Insecure | Redis Database (no auth by default) |
| 6443 | TCP | Kubernetes API | Containers | 🟢 Secure | Kubernetes API Server |
| 6667 | TCP | IRC | Messaging | 🔴 Insecure | Internet Relay Chat |
| 6697 | TCP | IRC-SSL | Messaging | 🟢 Secure | IRC over TLS/SSL |
| 6881 | TCP/UDP | BitTorrent | File Sharing | ⚪ Depends | BitTorrent (typical range 6881–6889) |
| 7001 | TCP | Cassandra-SSL | Database | 🟢 Secure | Cassandra SSL Inter-node |
| 7474 | TCP | Neo4j | Database | ⚪ Depends | Neo4j Browser/HTTP |
| 7687 | TCP | Bolt | Database | ⚪ Depends | Neo4j Bolt Protocol |
| 8080 | TCP | HTTP-Proxy | Web | 🔴 Insecure | HTTP Alternate / Proxy |
| 8086 | TCP | InfluxDB | Database | ⚪ Depends | InfluxDB HTTP API |
| 8091 | TCP | Couchbase | Database | ⚪ Depends | Couchbase Web Console |
| 8200 | TCP | Vault | Secrets Management | 🟢 Secure | HashiCorp Vault |
| 8291 | TCP | MikroTik Winbox | Network Admin | 🔴 Insecure | MikroTik RouterOS Winbox (frequent exploit target) |
| 8332 | TCP | Bitcoin-RPC | Cryptocurrency | ⚪ Depends | Bitcoin JSON-RPC |
| 8333 | TCP | Bitcoin | Cryptocurrency | ⚪ Depends | Bitcoin P2P Network |
| 8443 | TCP | HTTPS-Alt | Web | 🟢 Secure | Alternate HTTPS |
| 8500 | TCP | Consul | Service Discovery | ⚪ Depends | HashiCorp Consul Web UI |
| 8545 | TCP | Ethereum RPC | Cryptocurrency | 🔴 Insecure | Ethereum JSON-RPC |
| 8883 | TCP | MQTT-TLS | IoT / Messaging | 🟢 Secure | MQTT over TLS |
| 8888 | TCP | Jupyter | Development | ⚪ Depends | Jupyter Notebook |
| 8983 | TCP | Solr | Search | 🔴 Insecure | Apache Solr Admin |
| 9000 | TCP | PHP-FPM | Development | ⚪ Depends | PHP FastCGI / SonarQube |
| 9042 | TCP | Cassandra-CQL | Database | ⚪ Depends | Cassandra Native Client |
| 9050 | TCP | Tor-SOCKS | Anonymity | 🟢 Secure | Tor SOCKS Proxy |
| 9092 | TCP | Kafka | Messaging | ⚪ Depends | Apache Kafka Broker |
| 9200 | TCP | Elasticsearch | Database | 🔴 Insecure | Elasticsearch REST API (frequently exposed by mistake) |
| 9300 | TCP | Elasticsearch-Transport | Database | 🔴 Insecure | Elasticsearch Node Communication |
| 9418 | TCP | Git | Version Control | 🔴 Insecure | Git Protocol (unencrypted) |
| 10000 | TCP | Webmin | Admin Panel | ⚪ Depends | Webmin Admin Console |
| 10050 | TCP | Zabbix-Agent | Monitoring | 🔴 Insecure | Zabbix Agent |
| 10250 | TCP | Kubelet | Containers | ⚪ Depends | Kubernetes Kubelet API |
| 11211 | TCP/UDP | Memcached | Cache | 🔴 Insecure | Memcached (major amplification DDoS vector) |
| 15672 | TCP | RabbitMQ-Mgmt | Messaging | 🔴 Insecure | RabbitMQ Management UI |
| 25565 | TCP | Minecraft | Gaming | ⚪ Depends | Minecraft Java Edition |
| 27017 | TCP | MongoDB | Database | 🔴 Insecure | MongoDB Database (no auth by default — major risk) |
| 32400 | TCP | Plex | Media Server | ⚪ Depends | Plex Media Server |
| 44818 | TCP/UDP | EtherNet/IP | Industrial Control | 🔴 Insecure | Industrial EtherNet/IP (ICS/SCADA risk) |
| 47808 | UDP | BACnet | Industrial Control | 🔴 Insecure | Building Automation and Control (ICS risk) |

---

## Dynamic / Private Ports (49152–65535)

These ports are not assigned to any specific service by IANA and carry no fixed category/security profile — their risk depends entirely on what is bound to them.

| Range | Category | Security | Common Use |
|-------|----------|----------|-----------|
| 49152–65535 | Ephemeral | ⚪ Depends | OS-assigned client-side ports (Windows default) |
| 32768–60999 | Ephemeral | ⚪ Depends | Linux default ephemeral range |
| 1024–65535 | Ephemeral | ⚪ Depends | macOS/BSD default ephemeral range |

---

## Contributing

Found an error or want to add a port? Pull requests are welcome.

## License

This reference is provided under the [MIT License](https://opensource.org/licenses/MIT) — free to use, share, and modify.
