# 🌐 Linux Administration Task: Manage Networking

## Task List

- Create a connection with a static network configuration using the following:  
  - IP address: `172.25.250.11/24`  
  - Gateway address: `172.25.250.254`  
  - DNS address: `172.25.250.254`  

- Modify the new connection so that it also uses the IP address `10.0.1.1/24`.  

- Remove the connection.

---

# Additional Networking Exercises

## Lab Environment and Rules

- Complete these exercises on servera unless the instructor assigns a different host or interface.
- Work as root.
- Record active connection names, interfaces, addresses, routes, gateway, and DNS settings before changing them.
- Do not modify or delete the connection carrying the active remote-management session.
- Use a new training connection when an exercise asks you to create and later remove a profile.
- Connection profiles must contain the requested persistent settings and reactivate correctly after NetworkManager restart or reboot.

## Exercise 1

### Task List

- Save NetworkManager device and connection state, IPv4 addresses, routes, default gateway, DNS servers, and hostname in `/root/network-before.txt`.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `nmcli`, `ip address`, `ip route`, `resolvectl` or `/etc/resolv.conf`, `ping`, and a name-resolution test.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 2

### Task List

- Create connection `static-lab` on an instructor-designated unused interface with `172.25.250.11/24`, gateway `172.25.250.254`, DNS `172.25.250.254`, and manual IPv4 method.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `nmcli`, `ip address`, `ip route`, `resolvectl` or `/etc/resolv.conf`, `ping`, and a name-resolution test.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 3

### Task List

- Add `10.0.1.1/24` as a secondary IPv4 address on `static-lab` without removing `172.25.250.11/24`; activate and verify both addresses.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `nmcli`, `ip address`, `ip route`, `resolvectl` or `/etc/resolv.conf`, `ping`, and a name-resolution test.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 4

### Task List

- Create connection `dhcp-lab` on an unused interface using automatic IPv4 configuration, no static address, and autoconnect disabled.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `nmcli`, `ip address`, `ip route`, `resolvectl` or `/etc/resolv.conf`, `ping`, and a name-resolution test.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 5

### Task List

- Set the persistent hostname to the instructor-provided FQDN, verify it through hostnamectl, and confirm the host's primary address resolves locally.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `nmcli`, `ip address`, `ip route`, `resolvectl` or `/etc/resolv.conf`, `ping`, and a name-resolution test.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 6

### Task List

- Add DNS server `1.1.1.1` and search domain `example.com` to `static-lab` while preserving `172.25.250.254` as the first DNS server.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `nmcli`, `ip address`, `ip route`, `resolvectl` or `/etc/resolv.conf`, `ping`, and a name-resolution test.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 7

### Task List

- Add persistent route `192.0.2.0/24 via 172.25.250.254` to `static-lab`, verify route selection, then remove only that test route.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `nmcli`, `ip address`, `ip route`, `resolvectl` or `/etc/resolv.conf`, `ping`, and a name-resolution test.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 8

### Task List

- Enable autoconnect for `static-lab`, assign it an instructor-provided priority, restart NetworkManager, and confirm the intended profile activates.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `nmcli`, `ip address`, `ip route`, `resolvectl` or `/etc/resolv.conf`, `ping`, and a name-resolution test.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 9

### Task List

- Diagnose an instructor-created fault affecting address, route, DNS, or listening socket; record symptoms and final successful IP, route, ping, DNS, and socket tests.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `nmcli`, `ip address`, `ip route`, `resolvectl` or `/etc/resolv.conf`, `ping`, and a name-resolution test.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 10

### Task List

- Record every property required to recreate `static-lab`, delete only that profile, recreate it with identical settings, and prove equivalent connectivity.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `nmcli`, `ip address`, `ip route`, `resolvectl` or `/etc/resolv.conf`, `ping`, and a name-resolution test.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.
