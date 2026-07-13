| Port | Protocol | Service | Category | Security | Description |
|------|----------|---------|----------|----------|-------------|
| `20` | TCP | FTP Data | File Transfer | ❌ | FTP data channel |
| `21` | TCP | FTP | File Transfer | ❌ | File Transfer Protocol |
| `22`| TCP | SSH | Remote Access | ✅ | Secure Shell remote access |
| `23` | TCP | Telnet | Remote Access | ❌ | Remote terminal access |
| `25` | TCP | SMTP | Email | ❌ | Mail transfer protocol |
| `49` | TCP | TACACS+ | Authentication | ✅ | Network device authentication |
| `53` | TCP/UDP | DNS | Network | ❌ | Domain Name System |
| `67` | UDP | DHCP Server | Network | ❌ | Assigns IP addresses |
| `68` | UDP | DHCP Client | Network | ❌ | Receives IP configuration |
| `69` | UDP | TFTP | File Transfer | ❌ | Trivial File Transfer Protocol |
| `80` | TCP | HTTP | Web | ❌ | Hypertext Transfer Protocol |
| `88` | TCP/UDP | Kerberos | Authentication | ✅ | Authentication protocol |
| `110` | TCP | POP3 | Email | ❌ | Email retrieval |
| `111` | TCP/UDP | RPCbind | Network | ❌ | RPC service mapping |
| `119` | TCP | NNTP | News | ❌ | Network News Transfer Protocol |
| `123` | UDP | NTP | Time | ❌ | Network Time Protocol |
| `135` | TCP | MS RPC | Microsoft | ❌ | Remote Procedure Call |
| `137` | UDP | NetBIOS Name | Microsoft | ❌ | NetBIOS name service |
| `138` | UDP | NetBIOS Datagram | Microsoft | ❌ | NetBIOS datagram service |
| `139` | TCP | NetBIOS Session | Microsoft | ❌ | Windows file sharing |
| `143` | TCP | IMAP | Email | ❌ | Internet Message Access Protocol |
| `161` | UDP | SNMP | Monitoring | ❌ | Network monitoring |
| `162` | UDP | SNMP Trap | Monitoring | ❌ | SNMP notifications |
| `179` | TCP | BGP | Routing | ❌ | Border Gateway Protocol |
| `389` | TCP/UDP | LDAP | Directory | ❌ | Directory services |
| `443` | TCP | HTTPS | Web | ✅ | Secure HTTP |
| `445` | TCP | SMB | File Sharing | ❌ | Windows file sharing |
| `465` | TCP | SMTPS | Email | ✅ | Secure SMTP |
| `500` | UDP | IKE | VPN | ✅ | IPsec key exchange |
| `514` | UDP | Syslog | Logging | ❌ | System logging |
| `520` | UDP | RIP | Routing | ❌ | Routing Information Protocol |
| `587` | TCP | SMTP Submission | Email | ✅ | Secure mail submission |
| `631` | TCP | IPP | Printing | ❌ | Internet Printing Protocol |
| `636` | TCP | LDAPS | Directory | ✅ | Secure LDAP |
| `873` | TCP | rsync | File Transfer | ✅ | File synchronization |
| `989` | TCP | FTPS Data | File Transfer | ✅ | Secure FTP data |
| `990` | TCP | FTPS Control | File Transfer | ✅ | Secure FTP control |
| `993` | TCP | IMAPS | Email | ✅ | Secure IMAP |
| `995` | TCP | POP3S | Email | ✅ | Secure POP3 |
| `1080` | TCP | SOCKS Proxy | Proxy | Optional | SOCKS proxy server |
| `1194` | UDP | OpenVPN | VPN | ✅ | OpenVPN tunnel |
| `1433` | TCP | Microsoft SQL Server | Database | Optional | SQL Server database |
| `1434` | UDP | SQL Browser | Database | ❌ | SQL Server Browser |
| `1521` | TCP | Oracle Database | Database | Optional | Oracle listener |
| `1701` | UDP | L2TP | VPN | Optional | Layer 2 Tunneling Protocol |
| `1723` | TCP | PPTP | VPN | ❌ | Point-to-Point Tunneling Protocol |
| `1812` | UDP | RADIUS Authentication | Authentication | Optional | RADIUS authentication |
| `1813` | UDP | RADIUS Accounting | Authentication | Optional | RADIUS accounting |
| `2049` | TCP/UDP | NFS | File Sharing | ❌ | Network File System |
| `2375` | TCP | Docker API | Container | ❌ | Unencrypted Docker API |
| `2376` | TCP | Docker API TLS | Container | ✅ | Secure Docker API |
| `3306` | TCP | MySQL | Database | Optional | MySQL database |
| `3389` | TCP | RDP | Remote Access | ✅ | Remote Desktop Protocol |
| `3690` | TCP | Subversion | Version Control | Optional | SVN repository |
| `4369` | TCP | Erlang Port Mapper | Development | ❌ | Erlang node discovery |
| `5000` | TCP | Flask / Dev Server | Development | ❌ | Common development server |
| `5060` | TCP/UDP | SIP | VoIP | ❌ | Session Initiation Protocol |
| `5061` | TCP | SIP TLS | VoIP | ✅ | Secure SIP |
| `5432` | TCP | PostgreSQL | Database | Optional | PostgreSQL database |
| `5672` | TCP | RabbitMQ (AMQP) | Messaging | Optional | AMQP messaging |
| `5900` | TCP | VNC | Remote Access | Optional | Virtual Network Computing |
| `5985` | TCP | WinRM HTTP | Remote Access | ❌ | Windows Remote Management |
| `5986` | TCP | WinRM HTTPS | Remote Access | ✅ | Secure WinRM |
| `6379` | TCP | Redis | Database | Optional | Redis in-memory database |
| `6443` | TCP | Kubernetes API | Container | ✅ | Kubernetes API Server |
| `8080` | TCP | HTTP Alternate | Web | ❌ | Alternate HTTP |
| `8081` | TCP | HTTP Alternate | Web | ❌ | Alternative web service |
| `8443` | TCP | HTTPS Alternate | Web | ✅ | Alternative HTTPS |
| `9000` | TCP | SonarQube | Development | Optional | Code quality server |
| `9092` | TCP | Apache Kafka | Messaging | Optional | Kafka broker |
| `9200` | TCP | Elasticsearch | Search | Optional | Elasticsearch REST API |
| `9300` | TCP | Elasticsearch Cluster | Search | Optional | Cluster communication |
| `9418` | TCP | Git | Version Control | ❌ | Git native protocol |
| `10050` | TCP | Zabbix Agent | Monitoring | Optional | Zabbix monitoring agent |
| `10051` | TCP | Zabbix Server | Monitoring | Optional | Zabbix server |
| `11211` | TCP/UDP | Memcached | Cache | ❌ | Distributed memory cache |
| `15672` | TCP | RabbitMQ Management | Messaging | ✅ | RabbitMQ web management |
| `25565` | TCP | Minecraft Server | Gaming | Optional | Minecraft default server port |
| `27017` | TCP | MongoDB | Database | Optional | MongoDB database |
