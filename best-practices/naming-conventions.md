## 1. Linux User Naming Conventions (`useradd`)

### General Rules
- Use **lowercase only**
- No spaces
- No special characters (`@ ! # $ %`)
- Keep names short and deterministic
- Avoid uppercase (breaks scripts and SSH workflows)

---

### Human Users

Used for engineers, admins, and operators.

**Recommended patterns**
```

firstname
firstname.lastname
f.lastname
firstinitiallastname

```

**Examples**
```

arnav
arnav.srivastava
a.srivastava
asrivastava

```

**Why**
- Clean audit logs
- Easy SSH and sudo usage
- Compatible with LDAP / SSO

---

### Role-Based Admin Users

Used when responsibility is shared.

**Examples**
```

admin
sysadmin
devops
platform
sre

```

**Best Practice**
- Prefer individual logins + sudo
- Avoid shared passwords

---

### Service / Application Users (Highly Recommended)

Used by services and daemons.

**Patterns**
```

<service>
<service>user
svc_<service>
```

**Examples**

```
nginx
postgres
redis
svc_backup
svc_prometheus
```

**Why**

* Clear process ownership
* Clean file permissions
* Easy troubleshooting and auditing

---

### Avoid

```
DevOps
User123
john@company
app-user
```

---

## 2. Ansible Variable Naming Conventions

Ansible follows **Python and YAML standards**.

### General Rules

* Lowercase only
* Use `snake_case`
* No hyphens
* No camelCase
* Variables must be descriptive and scoped

---

### Simple Variables

```
app_name
app_port
db_host
db_user
```

---

### Role-Scoped Variables (Best Practice)

Prefix variables with role or component name.

```
nginx_port
nginx_user
nginx_worker_processes

postgres_db_name
postgres_db_user
postgres_data_dir
```

**Benefits**

* Prevents variable collisions
* Easier debugging
* Better readability

---

### Environment Variables

```
env
environment
deployment_env
```

**Examples**

```
env: prod
env: staging
env: dev
```

---

### Nested Variables (Recommended for Complex Configs)

```yaml
nginx:
  port: 80
  user: nginx
  worker_processes: 2
```

Accessed as:

```
nginx.port
nginx.user
```

**Why**

* Scales well
* Self-documenting
* Cleaner structure

---

### Avoid

```
AppPort
app-port
DBHOST
myVar
```

---

## 3. Hostname Naming Conventions (`hostnamectl`)

Hostnames directly impact **monitoring, automation, DNS, and observability**.

### Global Rules

* Lowercase only
* No underscores (RFC compliant)
* Use hyphens
* Predictable and searchable

---

### Recommended Pattern

```
<env>-<role>-<app>-<index>
```

---

### Examples

#### Application Servers

```
prod-web-frontend-01
prod-api-backend-02
staging-web-frontend-01
```

---

#### Database Servers

```
prod-db-postgres-01
prod-db-mysql-01
```

---

#### Kubernetes Nodes

```
prod-k8s-master-01
prod-k8s-worker-01
```

---

#### Monitoring and Infra

```
prod-monitor-prometheus-01
prod-logging-loki-01
```

---

### With Region or Datacenter

```
prod-in-web-frontend-01
prod-eu-db-postgres-01
```

---

### Avoid

```
Server1
MyVM
DB_SERVER
ProdServer
```

These cause issues with:

* DNS
* Monitoring labels
* Automation
* Human readability

---


```
```
