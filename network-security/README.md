# 🔐 Manage Network Security

## Objective

Configure network-level access for web services and validate accessibility from a remote machine.

## Task Steps

1. From the **controller** machine, test access to the default web server on `serverb`:

http://serverb.example.com


2. On the `serverb` machine, configure the **firewalld** service to allow the `httpd` service to listen on **port 82/TCP**.

3. From the **controller** machine, test access again — this time using the custom port:

http://serverb.example.com:82


> ✅ Ensure that all firewall changes are **permanent** and survive reboots.

---

# Additional Network Security Exercises

## Lab Environment and Rules

- Complete these exercises on serverb for firewall changes and controller for remote connectivity tests.
- Work as root on serverb and student on controller unless otherwise stated.
- Identify the active zone and its attached interface before changing firewalld.
- Preserve the classroom SSH connection and do not remove an existing rule required for management access.
- Apply changes to the permanent configuration and reload only after checking the requested rule.
- Every requested firewall rule must appear in the permanent configuration and still work after firewalld is reloaded or the host is rebooted.

## Exercise 1

### Task List

- Record the active firewalld zone, attached interfaces, sources, services, ports, masquerading state, and rich rules in `/root/firewall-before.txt`.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `firewall-cmd` runtime and permanent listings, `ss -lntup` on serverb, and `curl` or another remote connection test from controller.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 2

### Task List

- Add the predefined `http` service permanently to serverb's active zone, reload firewalld, and receive an HTTP response from `http://serverb.example.com` on controller.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `firewall-cmd` runtime and permanent listings, `ss -lntup` on serverb, and `curl` or another remote connection test from controller.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 3

### Task List

- Add TCP port 82 permanently, ensure httpd actually listens on port 82, reload firewalld, and retrieve `http://serverb.example.com:82` from controller.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `firewall-cmd` runtime and permanent listings, `ss -lntup` on serverb, and `curl` or another remote connection test from controller.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 4

### Task List

- Remove only TCP port 82 from the permanent zone, reload, confirm port 80 still works, and confirm a new connection to port 82 is blocked.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `firewall-cmd` runtime and permanent listings, `ss -lntup` on serverb, and `curl` or another remote connection test from controller.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 5

### Task List

- Create zone `classroom`, add source `172.25.250.0/24` permanently, and confirm firewalld selects that zone for traffic from the classroom subnet.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `firewall-cmd` runtime and permanent listings, `ss -lntup` on serverb, and `curl` or another remote connection test from controller.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 6

### Task List

- Add a permanent rich rule allowing SSH from `172.25.250.0/24`; remove the broad SSH service allowance only after proving controller remains able to connect.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `firewall-cmd` runtime and permanent listings, `ss -lntup` on serverb, and `curl` or another remote connection test from controller.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 7

### Task List

- Forward incoming TCP port 8080 to local TCP port 80 in the active zone; retrieve the default page through port 8080 from controller.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `firewall-cmd` runtime and permanent listings, `ss -lntup` on serverb, and `curl` or another remote connection test from controller.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 8

### Task List

- Enable masquerading permanently in zone `classroom`, reload firewalld, and record both runtime and permanent masquerade state before disabling it again if instructed.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `firewall-cmd` runtime and permanent listings, `ss -lntup` on serverb, and `curl` or another remote connection test from controller.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 9

### Task List

- Make one safe runtime-only test rule, compare runtime and permanent listings, use the supported operation to save runtime state permanently, and prove both listings match.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `firewall-cmd` runtime and permanent listings, `ss -lntup` on serverb, and `curl` or another remote connection test from controller.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 10

### Task List

- Create service `training-app` for TCP ports 9000 and 9001 using a custom service definition, add it permanently, reload, and confirm both ports appear through the service.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `firewall-cmd` runtime and permanent listings, `ss -lntup` on serverb, and `curl` or another remote connection test from controller.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.
