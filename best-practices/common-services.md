# Common Linux / Network Services Reference

This document lists commonly used services, their default ports, and primary configuration file locations (RHEL/CentOS/Ubuntu based systems).

---

## Web Servers

| Service | Default Port | Config File Path |
|----------|-------------|------------------|
| Apache (httpd) | 80 (HTTP), 443 (HTTPS) | /etc/httpd/conf/httpd.conf (RHEL/CentOS) <br> /etc/apache2/apache2.conf (Ubuntu/Debian) |
| Nginx | 80 (HTTP), 443 (HTTPS) | /etc/nginx/nginx.conf |
| Lighttpd | 80 | /etc/lighttpd/lighttpd.conf |

---

## Remote Access Services

| Service | Default Port | Config File Path |
|----------|-------------|------------------|
| SSH | 22 | /etc/ssh/sshd_config |
| Telnet | 23 | /etc/xinetd.d/telnet |
| VNC | 5900+ | /etc/vnc.conf |

---

## File Transfer Services

| Service | Default Port | Config File Path |
|----------|-------------|------------------|
| FTP (vsftpd) | 21 | /etc/vsftpd/vsftpd.conf |
| SFTP | 22 (via SSH) | /etc/ssh/sshd_config |
| TFTP | 69 | /etc/xinetd.d/tftp |

---

## Mail Services

| Service | Default Port | Config File Path |
|----------|-------------|------------------|
| SMTP (Postfix) | 25 | /etc/postfix/main.cf |
| SMTPS | 465 | /etc/postfix/main.cf |
| Submission (SMTP) | 587 | /etc/postfix/main.cf |
| POP3 | 110 | /etc/dovecot/dovecot.conf |
| IMAP | 143 | /etc/dovecot/dovecot.conf |
| IMAPS | 993 | /etc/dovecot/dovecot.conf |

---

## Database Services

| Service | Default Port | Config File Path |
|----------|-------------|------------------|
| MySQL | 3306 | /etc/my.cnf |
| MariaDB | 3306 | /etc/my.cnf |
| PostgreSQL | 5432 | /var/lib/pgsql/data/postgresql.conf |
| MongoDB | 27017 | /etc/mongod.conf |
| Redis | 6379 | /etc/redis.conf |

---

## DNS / Directory Services

| Service | Default Port | Config File Path |
|----------|-------------|------------------|
| DNS (BIND) | 53 | /etc/named.conf |
| DHCP | 67 (Server), 68 (Client) | /etc/dhcp/dhcpd.conf |
| LDAP | 389 | /etc/openldap/slapd.conf |
| LDAPS | 636 | /etc/openldap/slapd.conf |

---

## Container & Orchestration

| Service | Default Port | Config File Path |
|----------|-------------|------------------|
| Docker | 2375 (non-TLS), 2376 (TLS) | /etc/docker/daemon.json |
| Kubernetes API Server | 6443 | /etc/kubernetes/manifests/kube-apiserver.yaml |
| etcd | 2379 | /etc/kubernetes/manifests/etcd.yaml |

---

## Monitoring & Logging

| Service | Default Port | Config File Path |
|----------|-------------|------------------|
| Prometheus | 9090 | /etc/prometheus/prometheus.yml |
| Grafana | 3000 | /etc/grafana/grafana.ini |
| Loki | 3100 | /etc/loki/local-config.yaml |

---

## Proxy / Load Balancer

| Service | Default Port | Config File Path |
|----------|-------------|------------------|
| HAProxy | 80 / 443 | /etc/haproxy/haproxy.cfg |
| Squid Proxy | 3128 | /etc/squid/squid.conf |

---

# Notes

- Ports may be changed manually inside configuration files.
- Always verify active ports using:
  
```

ss -tulnp

```

- Always verify service status using:

```

systemctl status <service-name>

```

---

