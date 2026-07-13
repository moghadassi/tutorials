# Network Ports Reference

A comprehensive, ordered reference of TCP/UDP network ports — from the well-known range (0–1023) through registered (1024–49151) and commonly used dynamic/private ports.

## Table of Contents

- [Port Ranges Overview](#port-ranges-overview)
- [Well-Known Ports (0–1023)](#well-known-ports-0-1023)
- [Registered Ports (1024–49151)](#registered-ports-1024-49151)
- [Dynamic / Private Ports (49152–65535)](#dynamic--private-ports-49152-65535)
- [Quick Reference by Category](#quick-reference-by-category)
- [Contributing](#contributing)

---

## Port Ranges Overview

| Range | Name | Description |
|-------|------|-------------|
| 0–1023 | Well-Known / System Ports | Assigned by IANA to standard services, require root/admin privileges on most OSes |
| 1024–49151 | Registered Ports | Registered with IANA by software vendors for specific applications |
| 49152–65535 | Dynamic / Private / Ephemeral Ports | Used for temporary/client-side connections, not assigned to specific services |

---

## Well-Known Ports (0–1023)

| Port | Protocol | Service | Description |
|------|----------|---------|-------------|
| 0    | TCP/UDP | Reserved | Not used |
| 1    | TCP | TCPMUX | TCP Port Service Multiplexer |
| 5    | TCP | RJE | Remote Job Entry |
| 7    | TCP/UDP | Echo | Echo Protocol |
| 9    | TCP/UDP | Discard | Discard Protocol |
| 11   | TCP | SYSTAT | Active Users |
| 13   | TCP/UDP | Daytime | Daytime Protocol |
| 17   | TCP | QOTD | Quote of the Day |
| 18   | TCP/UDP | MSP | Message Send Protocol |
| 19   | TCP/UDP | Chargen | Character Generator |
| 20   | TCP | FTP-DATA | FTP Data Transfer |
| 21   | TCP | FTP | File Transfer Protocol (Control) |
| 22   | TCP | SSH | Secure Shell |
| 23   | TCP | Telnet | Telnet Protocol |
| 25   | TCP | SMTP | Simple Mail Transfer Protocol |
| 26   | TCP | RSFTP | Simple File Transfer |
| 37   | TCP/UDP | Time | Time Protocol |
| 39   | UDP | RLP | Resource Location Protocol |
| 42   | TCP/UDP | WINS | Host Name Server |
| 43   | TCP | WHOIS | WHOIS Protocol |
| 49   | TCP/UDP | TACACS | Login Host Protocol |
| 53   | TCP/UDP | DNS | Domain Name System |
| 67   | UDP | DHCP/BOOTP | DHCP Server |
| 68   | UDP | DHCP/BOOTP | DHCP Client |
| 69   | UDP | TFTP | Trivial File Transfer Protocol |
| 70   | TCP | Gopher | Gopher Protocol |
| 79   | TCP | Finger | Finger Protocol |
| 80   | TCP | HTTP | Hypertext Transfer Protocol |
| 88   | TCP/UDP | Kerberos | Kerberos Authentication |
| 101  | TCP | HOSTNAME | NIC Host Name Server |
| 102  | TCP | ISO-TSAP | ISO Transport Service |
| 105  | TCP | CCSO | CCSO Nameserver |
| 107  | TCP | RTelnet | Remote Telnet Service |
| 109  | TCP | POP2 | Post Office Protocol v2 |
| 110  | TCP | POP3 | Post Office Protocol v3 |
| 111  | TCP/UDP | RPCbind | ONC RPC / Portmapper |
| 113  | TCP | Ident | Identification Protocol |
| 115  | TCP | SFTP | Simple File Transfer Protocol |
| 117  | TCP | UUCP-PATH | UUCP Path Service |
| 119  | TCP | NNTP | Network News Transfer Protocol |
| 123  | UDP | NTP | Network Time Protocol |
| 135  | TCP/UDP | MS RPC | Microsoft RPC Endpoint Mapper |
| 137  | TCP/UDP | NetBIOS-NS | NetBIOS Name Service |
| 138  | TCP/UDP | NetBIOS-DGM | NetBIOS Datagram Service |
| 139  | TCP/UDP | NetBIOS-SSN | NetBIOS Session Service |
| 143  | TCP | IMAP | Internet Message Access Protocol |
| 152  | TCP/UDP | BFTP | Background File Transfer Protocol |
| 153  | TCP/UDP | SGMP | Simple Gateway Monitoring Protocol |
| 156  | TCP/UDP | SQL Service | SQL Service |
| 158  | TCP/UDP | PCMail | PCMail Server |
| 161  | UDP | SNMP | Simple Network Management Protocol |
| 162  | UDP | SNMP-Trap | SNMP Trap |
| 170  | TCP | Print-srv | Network PostScript |
| 175  | TCP | VMNET | VMNET |
| 179  | TCP | BGP | Border Gateway Protocol |
| 194  | TCP/UDP | IRC | Internet Relay Chat |
| 199  | TCP/UDP | SMUX | SNMP Unix Multiplexer |
| 201 | TCP/UDP | AppleTalk | AppleTalk Routing Maintenance |
| 209 | TCP/UDP | QMTP | Quick Mail Transfer Protocol |
| 210 | TCP/UDP | Z39.50 | ANSI Z39.50 |
| 213 | TCP/UDP | IPX | Internetwork Packet Exchange |
| 218 | TCP/UDP | MPP | Message Posting Protocol |
| 220 | TCP/UDP | IMAP3 | Interactive Mail Access Protocol v3 |
| 259 | TCP/UDP | ESRO | Efficient Short Remote Operations |
| 264 | TCP/UDP | BGMP | Border Gateway Multicast Protocol |
| 280 | TCP/UDP | HTTP-MGMT | HTTP Management |
| 308 | TCP | Novastor | Novastor Online Backup |
| 311 | TCP | ASIP-WebAdmin | Apple Web Administration |
| 318 | TCP/UDP | PKIX-TimeStamp | Time Stamp Protocol |
| 322 | TCP/UDP | RTSPS | RTSP over TLS |
| 323 | TCP/UDP | RPKI-RTR | RPKI to Router Protocol |
| 383 | TCP/UDP | HP-Data-Alarm | HP Data Alarm Manager |
| 384 | TCP/UDP | A-Remote | A Remote Network Server System |
| 387 | TCP/UDP | AURP | AppleTalk Update-based Routing |
| 389 | TCP/UDP | LDAP | Lightweight Directory Access Protocol |
| 401 | TCP/UDP | UPS | Uninterruptible Power Supply |
| 411 | TCP | Direct | Direct Connect Hub |
| 412 | TCP | TraceRoute | Trace Route |
| 427 | TCP/UDP | SLP | Service Location Protocol |
| 433 | TCP | NNSP | NNTP Multiplexer |
| 443 | TCP | HTTPS | HTTP Secure (TLS/SSL) |
| 444 | TCP/UDP | SNPP | Simple Network Paging Protocol |
| 445 | TCP | Microsoft-DS | SMB / Active Directory |
| 446 | TCP/UDP | DDM-RDB | DDM-RDB |
| 464 | TCP/UDP | Kpasswd | Kerberos Change/Set Password |
| 465 | TCP | SMTPS | SMTP over TLS (Submission) |
| 497 | TCP | Dantz | Retrospect Backup |
| 500 | UDP | ISAKMP/IKE | Internet Key Exchange (IPsec) |
| 512 | TCP | Exec | Remote Process Execution |
| 512 | UDP | Comsat/Biff | Comsat |
| 513 | TCP | Login | Remote Login (rlogin) |
| 513 | UDP | Who | Who Service |
| 514 | TCP | Shell | Remote Command (rsh) |
| 514 | UDP | Syslog | System Logging Protocol |
| 515 | TCP | LPD | Line Printer Daemon |
| 517 | UDP | Talk | Talk Protocol |
| 518 | UDP | Ntalk | New Talk Protocol |
| 520 | TCP | EFS | Extended File Name Server |
| 520 | UDP | RIP | Routing Information Protocol |
| 521 | UDP | RIPng | RIP Next Generation (IPv6) |
| 524 | TCP/UDP | NCP | NetWare Core Protocol |
| 525 | UDP | Timed | Time Daemon |
| 530 | TCP/UDP | RPC | Courier RPC |
| 531 | TCP/UDP | AOL/IRC | AOL Instant Messenger / IRC |
| 532 | TCP | Netnews | Network News |
| 533 | UDP | Netwall | Emergency Broadcasts |
| 540 | TCP | UUCP | Unix-to-Unix Copy Protocol |
| 542 | TCP/UDP | Commerce | Commerce Applications |
| 543 | TCP | Klogin | Kerberos Login |
| 544 | TCP | Kshell | Kerberos Remote Shell |
| 546 | TCP/UDP | DHCPv6-Client | DHCP for IPv6 Client |
| 547 | TCP/UDP | DHCPv6-Server | DHCP for IPv6 Server |
| 548 | TCP | AFP | Apple Filing Protocol |
| 550 | UDP | New-RWho | New Who |
| 554 | TCP/UDP | RTSP | Real Time Streaming Protocol |
| 556 | TCP | RFS | Remote File Share |
| 560 | UDP | RMonitor | Remote Monitor |
| 561 | UDP | Monitor | Monitor |
| 563 | TCP/UDP | NNTPS | NNTP over TLS |
| 587 | TCP | SMTP Submission | Email Message Submission |
| 591 | TCP | FileMaker | FileMaker HTTP Alternate |
| 593 | TCP/UDP | HTTP-RPC-EPMAP | HTTP RPC Endpoint Mapper |
| 601 | TCP | Syslog-Conn | Reliable Syslog Service |
| 623 | UDP | ASF-RMCP / IPMI | Alert Standard Forum / IPMI |
| 631 | TCP/UDP | IPP | Internet Printing Protocol / CUPS |
| 636 | TCP/UDP | LDAPS | LDAP over TLS/SSL |
| 639 | TCP/UDP | MSDP | Multicast Source Discovery Protocol |
| 646 | TCP/UDP | LDP | Label Distribution Protocol (MPLS) |
| 647 | TCP | DHCP-Failover | DHCP Failover |
| 648 | TCP | RRP | Registry Registrar Protocol |
| 651 | TCP/UDP | IEEE-MMS | IEEE MMS |
| 653 | TCP/UDP | SupportSoft | SupportSoft Nexus |
| 654 | TCP | AODV | Ad-hoc On-demand Distance Vector |
| 660 | TCP | Mac-SrvrAdmin | Apple Server Admin |
| 665 | TCP/UDP | SUN-DR | Sun DR |
| 674 | TCP/UDP | ACAP | Application Config Access Protocol |
| 691 | TCP | MS-Exchange | MS Exchange Routing |
| 694 | TCP/UDP | HA-Cluster | Linux-HA Heartbeat |
| 695 | TCP/UDP | IEEE-MMS-SSL | IEEE MMS over SSL |
| 698 | UDP | OLSR | Optimized Link State Routing |
| 700 | TCP | EPP | Extensible Provisioning Protocol |
| 701 | TCP | LMP | Link Management Protocol |
| 702 | TCP | IRIS-BEEP | IRIS over BEEP |
| 706 | TCP | SILC | Secure Internet Live Conferencing |
| 711 | TCP | Cisco-TDP | Cisco Tag Distribution Protocol |
| 712 | TCP/UDP | TBRPF | Topology Broadcast Reverse Path |
| 720 | TCP | SMQP | Smooth Message Queue Protocol |
| 749 | TCP/UDP | Kerberos-ADM | Kerberos Administration |
| 750 | TCP/UDP | Kerberos-IV | Kerberos v4 |
| 765 | TCP/UDP | Webster | Network Dictionary |
| 767 | TCP | Phonebook | Phone Book |
| 775 | TCP | ENTOMB | Moira Update Protocol |
| 777 | TCP/UDP | MultiLing-HTTP | Multiling HTTP |
| 783 | TCP | Spamassassin | SpamAssassin Spam Daemon |
| 800 | TCP/UDP | mdbs_daemon | MDBS Daemon |
| 808 | TCP | Omirr | Omirr / Omvia |
| 843 | TCP | Flash-Policy | Adobe Flash Socket Policy |
| 847 | TCP/UDP | Dhcp-Failover2 | DHCP Failover v2 |
| 848 | TCP/UDP | GDOI | Group Domain of Interpretation |
| 860 | TCP | iSCSI | iSCSI Protocol |
| 873 | TCP | Rsync | Remote Sync Protocol |
| 888 | TCP | CDDBP | CD Database Protocol |
| 902 | TCP/UDP | VMware-Auth | VMware Server Authentication |
| 903 | TCP | VMware | VMware Remote Console |
| 904 | TCP | VMware-Alt | VMware Alt |
| 911 | TCP | NCA | Network Console Access |
| 981 | TCP | SofaWare | Check Point HTTPS Management |
| 989 | TCP | FTPS-Data | FTP over TLS (Data) |
| 990 | TCP | FTPS | FTP over TLS (Control) |
| 991 | TCP | NAS | Netnews Administration System |
| 992 | TCP/UDP | Telnets | Telnet over TLS/SSL |
| 993 | TCP | IMAPS | IMAP over TLS/SSL |
| 995 | TCP | POP3S | POP3 over TLS/SSL |
| 999 | TCP | Garcon | Garcon / SCP |
| 1000 | TCP | Cadlock | Cadlock |
| 1010 | TCP | Surf | Surf |
| 1023 | TCP/UDP | Reserved | Last Well-Known Port |

---

## Registered Ports (1024–49151)

> This range contains 48,000+ ports. Below are the most commonly encountered ones in real-world networking, development, and security contexts.

| Port | Protocol | Service | Description |
|------|----------|---------|-------------|
| 1025 | TCP/UDP | NFS-or-IIS | Microsoft RPC / IIS |
| 1080 | TCP | SOCKS | SOCKS Proxy |
| 1099 | TCP | RMI Registry | Java RMI Registry |
| 1109 | TCP | KPOP | Kerberos POP |
| 1167 | UDP | Phone | Conference Calling |
| 1194 | TCP/UDP | OpenVPN | OpenVPN |
| 1214 | TCP | Kazaa | Kazaa File Sharing |
| 1241 | TCP/UDP | Nessus | Nessus Vulnerability Scanner |
| 1311 | TCP | RxMon | ImageCast RxMon |
| 1337 | TCP | WASTE | WASTE Encrypted File Sharing |
| 1352 | TCP | Lotus Notes | IBM Lotus Notes |
| 1433 | TCP | MS-SQL | Microsoft SQL Server |
| 1434 | UDP | MS-SQL-Monitor | MS SQL Monitor |
| 1494 | TCP | Citrix ICA | Citrix Independent Computing Architecture |
| 1512 | TCP/UDP | WINS | Microsoft Windows Internet Name Service |
| 1521 | TCP | Oracle DB | Oracle Database Listener |
| 1524 | TCP | Ingreslock | Ingres Lock / Common Backdoor |
| 1526 | TCP | Oracle DB Alt | Oracle Database Alternate |
| 1533 | TCP | Sametime | IBM Sametime |
| 1547 | TCP | LaplinK | Laplink |
| 1550 | TCP | Gadu-Gadu | Gadu-Gadu Messenger |
| 1583 | TCP | Simbaservices | Simba Services |
| 1589 | TCP | Cisco VQP | Cisco VLAN Query Protocol |
| 1701 | UDP | L2TP | Layer 2 Tunneling Protocol |
| 1720 | TCP | H.323 | H.323 Call Signaling |
| 1723 | TCP | PPTP | Point-to-Point Tunneling Protocol |
| 1725 | UDP | Steam | Steam Friends Network |
| 1755 | TCP/UDP | MMS | Microsoft Media Services |
| 1761 | TCP | CFTP | Cisco Fault Tolerant Protocol |
| 1812 | UDP | RADIUS | RADIUS Authentication |
| 1813 | UDP | RADIUS-Acct | RADIUS Accounting |
| 1863 | TCP | MSNP | MSN Messenger |
| 1900 | UDP | SSDP | Simple Service Discovery Protocol |
| 1935 | TCP | RTMP | Real Time Messaging Protocol |
| 1985 | UDP | HSRP | Hot Standby Router Protocol |
| 2000 | TCP | Cisco SCCP | Skinny Client Control Protocol |
| 2049 | TCP/UDP | NFS | Network File System |
| 2082 | TCP | cPanel | cPanel Default |
| 2083 | TCP | cPanel-SSL | cPanel over SSL |
| 2086 | TCP | WHM | Web Host Manager |
| 2087 | TCP | WHM-SSL | Web Host Manager over SSL |
| 2095 | TCP | Webmail | cPanel Webmail |
| 2096 | TCP | Webmail-SSL | cPanel Webmail over SSL |
| 2100 | TCP | Amiganetfs | Amiga Network Filesystem |
| 2181 | TCP | ZooKeeper | Apache ZooKeeper Client Port |
| 2222 | TCP | DirectAdmin/SSH-Alt | DirectAdmin Panel / Alternate SSH |
| 2302 | UDP | ArmA | ArmA Game Server |
| 2375 | TCP | Docker | Docker REST API (unencrypted) |
| 2376 | TCP | Docker-TLS | Docker REST API over TLS |
| 2377 | TCP | Docker Swarm | Docker Swarm Cluster Management |
| 2379 | TCP | etcd-client | etcd Client Communication |
| 2380 | TCP | etcd-peer | etcd Peer Communication |
| 2401 | TCP | CVS | Concurrent Versions System |
| 2483 | TCP/UDP | Oracle-DB | Oracle DB (unencrypted) |
| 2484 | TCP/UDP | Oracle-DB-SSL | Oracle DB over SSL |
| 2967 | TCP | Symantec AV | Symantec System Center |
| 3000 | TCP | Dev-Server | Common Dev Server (Node/Rails/etc.) |
| 3001 | TCP | Dev-Server-Alt | Alternate Dev Server |
| 3037 | TCP | HP Data Protector | HP Data Protector |
| 3050 | TCP | Firebird | Firebird Database |
| 3074 | TCP/UDP | Xbox Live | Xbox Live / Games for Windows |
| 3128 | TCP | Squid Proxy | Squid Web Proxy |
| 3260 | TCP | iSCSI-Target | iSCSI Target |
| 3268 | TCP | LDAP-GC | Microsoft Global Catalog |
| 3269 | TCP | LDAP-GC-SSL | Global Catalog over SSL |
| 3283 | TCP/UDP | Apple Remote Desktop | Apple Remote Desktop |
| 3306 | TCP | MySQL | MySQL Database |
| 3307 | TCP | MySQL-Alt | MySQL Alternate |
| 3389 | TCP | RDP | Remote Desktop Protocol |
| 3396 | TCP | Novell NDPS | Novell Distributed Print |
| 3689 | TCP | DAAP | Digital Audio Access Protocol (iTunes) |
| 3690 | TCP | SVN | Subversion Version Control |
| 3724 | TCP/UDP | WoW | World of Warcraft |
| 3784 | TCP/UDP | Ventrilo | Ventrilo Voice Chat |
| 3785 | UDP | Ventrilo-Alt | Ventrilo Alternate |
| 4000 | TCP | ICQ | ICQ Protocol |
| 4040 | TCP | Spark Web UI | Apache Spark Web UI |
| 4111 | TCP | Xgrid | Apple Xgrid |
| 4200 | TCP | Angular Dev Server | Angular CLI Dev Server |
| 4443 | TCP | Pharos/HTTPS-Alt | Alternate HTTPS |
| 4444 | TCP | Metasploit/Blaster | Common Backdoor / Metasploit Default |
| 4500 | UDP | IPsec-NAT-T | IPsec NAT Traversal |
| 4664 | TCP | Google Desktop | Google Desktop Search |
| 4672 | UDP | eMule | eMule File Sharing |
| 4899 | TCP | Radmin | Remote Administrator |
| 5000 | TCP | UPnP/Flask-Dev | Universal Plug and Play / Flask Dev Server |
| 5001 | TCP | Synology/Slingbox | Synology DSM / Slingbox |
| 5004 | TCP/UDP | RTP | Real-time Transport Protocol |
| 5005 | TCP/UDP | RTP-Alt | Real-time Transport Protocol Alt |
| 5050 | TCP | Yahoo Messenger | Yahoo Messenger |
| 5060 | TCP/UDP | SIP | Session Initiation Protocol |
| 5061 | TCP | SIPS | SIP over TLS |
| 5100 | TCP | SOCKS-Alt | Service Location Protocol Alt |
| 5190 | TCP | AIM/ICQ | AOL Instant Messenger |
| 5222 | TCP | XMPP-Client | XMPP / Jabber Client |
| 5223 | TCP | XMPP-SSL | XMPP over SSL |
| 5228 | TCP | Google Play | Android Google Play/GCM |
| 5269 | TCP | XMPP-Server | XMPP Server-to-Server |
| 5353 | UDP | mDNS | Multicast DNS (Bonjour) |
| 5355 | TCP/UDP | LLMNR | Link-Local Multicast Name Resolution |
| 5432 | TCP | PostgreSQL | PostgreSQL Database |
| 5433 | TCP | PostgreSQL-Alt | PostgreSQL Alternate |
| 5555 | TCP | Android Debug Bridge | ADB / Freeciv |
| 5601 | TCP | Kibana | Kibana Web Interface |
| 5631 | TCP | pcAnywhere | pcAnywhere Data |
| 5632 | UDP | pcAnywhere-Stat | pcAnywhere Status |
| 5666 | TCP | NRPE | Nagios Remote Plugin Executor |
| 5672 | TCP | AMQP | Advanced Message Queuing Protocol (RabbitMQ) |
| 5683 | UDP | CoAP | Constrained Application Protocol |
| 5900 | TCP | VNC | Virtual Network Computing |
| 5901 | TCP | VNC-1 | VNC Display :1 |
| 5938 | TCP | TeamViewer | TeamViewer Remote Access |
| 5984 | TCP | CouchDB | Apache CouchDB |
| 5985 | TCP | WinRM-HTTP | Windows Remote Management |
| 5986 | TCP | WinRM-HTTPS | Windows Remote Management over TLS |
| 6000 | TCP | X11 | X Window System |
| 6379 | TCP | Redis | Redis Database |
| 6443 | TCP | Kubernetes API | Kubernetes API Server |
| 6446 | TCP | MySQL-Proxy | MySQL Proxy |
| 6500 | TCP | GameSpy Arcade | GameSpy Arcade |
| 6566 | TCP | SANE | SANE Scanner Network Daemon |
| 6588 | TCP | AnalogX | AnalogX Proxy |
| 6600 | TCP | MPD | Music Player Daemon |
| 6619 | TCP | ODETTE-FTP | ODETTE File Transfer Protocol |
| 6660 | TCP | IRC-Alt | Alternate IRC |
| 6667 | TCP | IRC | Internet Relay Chat |
| 6697 | TCP | IRC-SSL | IRC over TLS/SSL |
| 6699 | TCP | Napster | Napster |
| 6881 | TCP/UDP | BitTorrent | BitTorrent (typical range 6881–6889) |
| 6969 | TCP/UDP | BitTorrent-Tracker | BitTorrent Tracker |
| 7000 | TCP | Cassandra | Apache Cassandra Inter-node |
| 7001 | TCP | Cassandra-SSL | Cassandra SSL Inter-node |
| 7070 | TCP | RealAudio | RealAudio Streaming |
| 7077 | TCP | Spark Master | Apache Spark Master |
| 7199 | TCP | Cassandra-JMX | Cassandra JMX Monitoring |
| 7474 | TCP | Neo4j | Neo4j Browser/HTTP |
| 7687 | TCP | Bolt | Neo4j Bolt Protocol |
| 7777 | TCP/UDP | Game Servers | Common Game Server Port |
| 8000 | TCP | HTTP-Alt | Common Alternate HTTP |
| 8001 | TCP | HTTP-Alt2 | Alternate HTTP |
| 8008 | TCP | HTTP-Alt3 | Alternate HTTP / Chromecast |
| 8009 | TCP | AJP13 | Apache JServ Protocol (Tomcat) |
| 8080 | TCP | HTTP-Proxy | HTTP Alternate / Proxy |
| 8081 | TCP | HTTP-Alt4 | Alternate HTTP |
| 8086 | TCP | InfluxDB | InfluxDB HTTP API |
| 8087 | TCP | Riak | Riak Protocol Buffers |
| 8091 | TCP | Couchbase | Couchbase Web Console |
| 8095 | TCP | Jenkins-Alt | Alternate Jenkins |
| 8096 | TCP | Jellyfin | Jellyfin Media Server |
| 8112 | TCP | Deluge | Deluge Torrent Web UI |
| 8123 | TCP | Home Assistant | Home Assistant Web UI |
| 8140 | TCP | Puppet | Puppet Master |
| 8161 | TCP | ActiveMQ | ActiveMQ Web Console |
| 8200 | TCP | Vault | HashiCorp Vault |
| 8222 | TCP | VMware Server | VMware Server Management |
| 8280 | TCP | HTTP-Alt5 | Apache Synapse |
| 8291 | TCP | MikroTik Winbox | MikroTik RouterOS Winbox |
| 8332 | TCP | Bitcoin-RPC | Bitcoin JSON-RPC |
| 8333 | TCP | Bitcoin | Bitcoin P2P Network |
| 8443 | TCP | HTTPS-Alt | Alternate HTTPS |
| 8500 | TCP | Consul | HashiCorp Consul Web UI |
| 8530 | TCP | WSUS | Windows Server Update Services |
| 8531 | TCP | WSUS-SSL | WSUS over SSL |
| 8545 | TCP | Ethereum RPC | Ethereum JSON-RPC |
| 8546 | TCP | Ethereum WS | Ethereum WebSocket |
| 8600 | TCP/UDP | Consul-DNS | Consul DNS Interface |
| 8649 | TCP/UDP | Ganglia | Ganglia Monitoring |
| 8800 | TCP | Sun Web Admin | Sun Web Admin Console |
| 8834 | TCP | Nessus-Web | Nessus Web Interface |
| 8880 | TCP | CDDBP-Alt | Alternate CDDBP |
| 8883 | TCP | MQTT-TLS | MQTT over TLS |
| 8888 | TCP | HTTP-Alt6 | Jupyter Notebook / Common Alt HTTP |
| 8983 | TCP | Solr | Apache Solr Admin |
| 9000 | TCP | PHP-FPM | PHP FastCGI Process Manager / SonarQube |
| 9001 | TCP | Supervisor/Tor | Supervisor Web UI / Tor ORPort |
| 9042 | TCP | Cassandra-CQL | Cassandra Native Client |
| 9050 | TCP | Tor-SOCKS | Tor SOCKS Proxy |
| 9051 | TCP | Tor-Control | Tor Control Port |
| 9060 | TCP | WAS-Admin | WebSphere Admin Console |
| 9080 | TCP | WAS-HTTP | WebSphere HTTP |
| 9090 | TCP | Prometheus/WebSM | Prometheus Web UI / Openfire Admin |
| 9091 | TCP | Transmission | Transmission Torrent Web UI |
| 9092 | TCP | Kafka | Apache Kafka Broker |
| 9100 | TCP | JetDirect/Node-Exporter | Printer Port / Prometheus Node Exporter |
| 9200 | TCP | Elasticsearch | Elasticsearch REST API |
| 9300 | TCP | Elasticsearch-Transport | Elasticsearch Node Communication |
| 9418 | TCP | Git | Git Protocol (unencrypted) |
| 9999 | TCP | Urchin/Abyss | Urchin Web Analytics |
| 10000 | TCP | Webmin | Webmin Admin Console |
| 10050 | TCP | Zabbix-Agent | Zabbix Agent |
| 10051 | TCP | Zabbix-Server | Zabbix Server |
| 10250 | TCP | Kubelet | Kubernetes Kubelet API |
| 10255 | TCP | Kubelet-RO | Kubernetes Kubelet Read-Only |
| 11211 | TCP/UDP | Memcached | Memcached Distributed Caching |
| 11371 | TCP | HKP | OpenPGP HTTP Keyserver |
| 12345 | TCP | NetBus | NetBus Backdoor (historical) |
| 15672 | TCP | RabbitMQ-Mgmt | RabbitMQ Management UI |
| 16379 | TCP | Redis-Cluster | Redis Cluster Bus |
| 16992 | TCP | Intel AMT | Intel Active Management Technology |
| 17500 | TCP/UDP | Dropbox LAN Sync | Dropbox LAN Sync Discovery |
| 18080 | TCP | Monero | Monero P2P Network |
| 19132 | UDP | Minecraft Bedrock | Minecraft Bedrock Edition |
| 20000 | TCP | Usermin | Usermin Admin Console |
| 24800 | TCP/UDP | Synergy | Synergy KVM Software |
| 25565 | TCP | Minecraft | Minecraft Java Edition |
| 27015 | TCP/UDP | Source Engine | Valve Source Engine Games |
| 27017 | TCP | MongoDB | MongoDB Database |
| 27018 | TCP | MongoDB-Shard | MongoDB Shard Server |
| 27019 | TCP | MongoDB-Config | MongoDB Config Server |
| 28015 | TCP | RethinkDB | RethinkDB Client Driver |
| 28017 | TCP | MongoDB-Web | MongoDB Web Status |
| 32400 | TCP | Plex | Plex Media Server |
| 33060 | TCP | MySQL-X | MySQL X Protocol |
| 37777 | TCP | DVR | Common DVR/CCTV Port |
| 41794 | TCP | Crestron | Crestron Control |
| 44818 | TCP/UDP | EtherNet/IP | Industrial EtherNet/IP |
| 47808 | UDP | BACnet | Building Automation and Control |
| 49151 | TCP/UDP | Reserved | Last Registered Port |

---

## Dynamic / Private Ports (49152–65535)

These ports are not assigned to any specific service by IANA. They are used as:

- **Ephemeral ports**: temporary source ports chosen by an OS for outgoing client connections
- **Custom application ports**: used by developers/admins for private services
- **NAT/firewall traversal**: often used in P2P and gaming connections

| Range | Common Use |
|-------|-----------|
| 49152–65535 | OS-assigned ephemeral ports (Windows default: 49152–65535) |
| 32768–60999 | Linux default ephemeral range (`/proc/sys/net/ipv4/ip_local_port_range`) |
| 1024–65535 | macOS/BSD default ephemeral range |

---

## Quick Reference by Category

### Web
`80` HTTP · `443` HTTPS · `8080` HTTP-Alt · `8443` HTTPS-Alt · `3000` Dev Server

### Email
`25` SMTP · `465` SMTPS · `587` Submission · `110` POP3 · `995` POP3S · `143` IMAP · `993` IMAPS

### File Transfer
`20/21` FTP · `22` SFTP (via SSH) · `989/990` FTPS · `69` TFTP · `873` Rsync

### Remote Access
`22` SSH · `23` Telnet · `3389` RDP · `5900` VNC · `5985/5986` WinRM

### Databases
`3306` MySQL · `5432` PostgreSQL · `1433` MS-SQL · `1521` Oracle · `27017` MongoDB · `6379` Redis · `9042` Cassandra · `5984` CouchDB

### DNS / Directory
`53` DNS · `389` LDAP · `636` LDAPS · `88` Kerberos

### Containers / Orchestration
`2375/2376` Docker · `2377` Docker Swarm · `6443` Kubernetes API · `10250` Kubelet · `2379/2380` etcd

### Messaging / Streaming
`5672` AMQP · `9092` Kafka · `1883/8883` MQTT · `5222` XMPP

### Monitoring
`9090` Prometheus · `9100` Node Exporter · `3000` Grafana (common alt) · `10050/10051` Zabbix

### VPN / Tunneling
`500` IKE · `1194` OpenVPN · `1701` L2TP · `1723` PPTP · `4500` IPsec NAT-T

---

## Contributing

Found an error or want to add a port? Pull requests are welcome.

## License

This reference is provided under the [MIT License](https://opensource.org/licenses/MIT) — free to use, share, and modify.
