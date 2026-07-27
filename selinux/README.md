# 🔐 Linux Administration Task: Manage SELinux Security

## Task List

- Your company has decided to run an `httpd` service, which listens on port `80/TCP`.  
- You should also make port `82/TCP` available for `httpd` access.  
- Configure SELinux to allow the `httpd` service to listen on port `82/TCP`.  
- All changes must **persist across a reboot**.

---

# Additional SELinux Exercises

## Lab Environment and Rules

- Complete these exercises on serverb.
- Work as root.
- Keep SELinux in enforcing mode; do not use disabling or permanent permissive mode as a solution.
- Inspect audit evidence and existing policy before adding a port, file context, or boolean.
- Use persistent policy-management commands rather than relying only on a temporary `chcon` label.
- File contexts, port labels, and boolean changes must survive relabeling and reboot.

## Exercise 1

### Task List

- Record `getenforce`, detailed SELinux status, active policy name, and configured boot mode in `/root/selinux-status.txt`; the final mode must remain enforcing.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `getenforce`, `sestatus`, `ls -Z`, `semanage`, `restorecon`, `getsebool`, `ausearch`, and a real service-access test.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 2

### Task List

- Save contexts for `/var/www`, `/var/www/html`, and all existing files directly below the document root; identify user, role, type, and level fields.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `getenforce`, `sestatus`, `ls -Z`, `semanage`, `restorecon`, `getsebool`, `ausearch`, and a real service-access test.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 3

### Task List

- Create `/tmp/context-test.html`, copy it and move a second copy into `/var/www/html`, compare labels, then restore the expected labels recursively.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `getenforce`, `sestatus`, `ls -Z`, `semanage`, `restorecon`, `getsebool`, `ausearch`, and a real service-access test.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 4

### Task List

- Create `/srv/website`, assign persistent type `httpd_sys_content_t` to the directory tree, apply the mapping, and prove a new file receives the intended type.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `getenforce`, `sestatus`, `ls -Z`, `semanage`, `restorecon`, `getsebool`, `ausearch`, and a real service-access test.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 5

### Task List

- Add TCP port 82 to SELinux type `http_port_t`, configure httpd to listen on it, and obtain a page on port 82 while SELinux is enforcing.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `getenforce`, `sestatus`, `ls -Z`, `semanage`, `restorecon`, `getsebool`, `ausearch`, and a real service-access test.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 6

### Task List

- List every TCP and UDP port currently mapped to `http_port_t`, save the result to `/root/http-ports.txt`, and confirm ports 80 and 82 are present.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `getenforce`, `sestatus`, `ls -Z`, `semanage`, `restorecon`, `getsebool`, `ausearch`, and a real service-access test.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 7

### Task List

- Generate or use an instructor-provided AVC denial, query recent AVC records with complete context, and save the relevant event in `/root/avc-denial.txt`.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `getenforce`, `sestatus`, `ls -Z`, `semanage`, `restorecon`, `getsebool`, `ausearch`, and a real service-access test.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 8

### Task List

- Analyze the recorded denial with installed SELinux troubleshooting tools and document the suggested cause; do not automatically install a generated allow module.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `getenforce`, `sestatus`, `ls -Z`, `semanage`, `restorecon`, `getsebool`, `ausearch`, and a real service-access test.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 9

### Task List

- For an instructor-provided web scenario, identify the narrow existing boolean, enable it persistently, and record its old and new state.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `getenforce`, `sestatus`, `ls -Z`, `semanage`, `restorecon`, `getsebool`, `ausearch`, and a real service-access test.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 10

### Task List

- Apply an incorrect temporary type to a test web file, demonstrate denied access, repair it with persistent mapping and restorecon, reboot, and demonstrate successful access.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `getenforce`, `sestatus`, `ls -Z`, `semanage`, `restorecon`, `getsebool`, `ausearch`, and a real service-access test.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.
