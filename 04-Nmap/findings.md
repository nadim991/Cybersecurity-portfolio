# Nmap Findings

## Target

IP Address: 192.168.196.129

The target is a Metasploitable virtual machine running in a VMware environment.

## Host Discovery

The host was found to be active.

MAC Address:
00:0C:29:E6:B1:99

Network Distance:
1 hop

## Open Ports

The scan identified the following open TCP ports:

| Port | Service | Version |
|------|---------|---------|
| 21 | FTP | vsftpd 2.3.4 |
| 22 | SSH | OpenSSH 4.7p1 |
| 23 | Telnet | Linux telnetd |
| 25 | SMTP | Postfix smtpd |
| 53 | DNS | ISC BIND 9.4.2 |
| 80 | HTTP | Apache 2.2.8 |
| 111 | RPC | rpcbind |
| 139 | NetBIOS | Samba |
| 445 | SMB | Samba |
| 512 | Rexec | netkit-rsh |
| 513 | Rlogin | OpenBSD/Solaris rlogind |
| 514 | Shell | tcpwrapped |
| 1099 | Java RMI | GNU Classpath grmiregistry |
| 1524 | Bindshell | Metasploitable root shell |
| 2049 | NFS | RPC #100003 |
| 2121 | FTP | ProFTPD 1.3.1 |
| 3306 | MySQL | MySQL 5.0.51a |
| 5432 | PostgreSQL | PostgreSQL 8.3.x |
| 5900 | VNC | Protocol 3.3 |
| 6000 | X11 | Access denied |
| 6667 | IRC | UnrealIRCd |
| 8009 | AJP13 | Apache Jserv |
| 8180 | HTTP | Apache Tomcat |

## Operating System Detection

Nmap identified the target as:

OS Family:
Linux

Kernel:
Linux 2.6.x

Estimated version:
Linux 2.6.9 - 2.6.33

Device Type:
General purpose

## Important Observations

The target exposes a large number of network services.

Several services are running older software versions.

The following services require further security assessment:

FTP
Telnet
SSH
HTTP
SMB
Rexec
Rlogin
Java RMI
NFS
MySQL
PostgreSQL
VNC
IRC
Apache Tomcat

Port 1524 was identified as a Metasploitable root shell.

## Conclusion

The Nmap assessment successfully identified the live host, open ports, running services, software versions, and probable operating system.

The results provide a foundation for further vulnerability assessment and penetration testing in the authorized lab environment.