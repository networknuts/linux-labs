# 🛠️ Linux Administration Task: Control Services

## Task List

1. Start the `sshd` service.  
2. Configure the `httpd` service to start at system boot.  
3. Stop the `rsyslog` service.  
4. Configure the `rsyslog` service so that it does not start at system boot.

---

# Additional Service Management Exercises

## Lab Environment and Rules

- Complete these exercises on servera unless the exercise names another machine.
- Work as root.
- Inspect the current active and enabled states before changing a service.
- Use reload instead of restart when an exercise requires uninterrupted service and the unit supports reload.
- Do not mask essential boot, networking, SSH, or logging services.
- Enabled, disabled, or masked states must remain correct after reboot when the exercise requests a boot-time behavior.

## Exercise 1

### Task List

- Create `/root/service-state.txt` showing active, enabled, and failed state for `sshd`, `httpd`, and `rsyslog` before any changes.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `systemctl status`, `systemctl is-active`, `systemctl is-enabled`, `systemctl show`, `ss -lntup`, and relevant journal messages.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 2

### Task List

- Start sshd without changing its boot-enabled state; prove the unit is active and a process is listening on its configured TCP port.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `systemctl status`, `systemctl is-active`, `systemctl is-enabled`, `systemctl show`, `ss -lntup`, and relevant journal messages.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 3

### Task List

- Stop httpd and prove its listener disappears, start it and retrieve a page locally, then restart it and confirm the main process ID changes.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `systemctl status`, `systemctl is-active`, `systemctl is-enabled`, `systemctl show`, `ss -lntup`, and relevant journal messages.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 4

### Task List

- Make an instructor-provided safe configuration change to a reload-capable service, reload without stopping it, and confirm the main process ID remains unchanged.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `systemctl status`, `systemctl is-active`, `systemctl is-enabled`, `systemctl show`, `ss -lntup`, and relevant journal messages.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 5

### Task List

- Enable httpd for boot, inspect the created target dependency, reboot, and prove httpd is active without a manual start.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `systemctl status`, `systemctl is-active`, `systemctl is-enabled`, `systemctl show`, `ss -lntup`, and relevant journal messages.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 6

### Task List

- Leave rsyslog running now but disable it for future boots; prove active state is `active` while enabled state is `disabled` before reboot.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `systemctl status`, `systemctl is-active`, `systemctl is-enabled`, `systemctl show`, `ss -lntup`, and relevant journal messages.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 7

### Task List

- Use only the instructor-designated disposable unit for masking; show that manual start fails while masked and save the exact failure message.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `systemctl status`, `systemctl is-active`, `systemctl is-enabled`, `systemctl show`, `ss -lntup`, and relevant journal messages.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 8

### Task List

- Unmask the disposable unit, restore the enabled state recorded before masking, start it successfully, and confirm no failed-unit state remains.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `systemctl status`, `systemctl is-active`, `systemctl is-enabled`, `systemctl show`, `ss -lntup`, and relevant journal messages.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 9

### Task List

- Save the complete unit definition and selected properties `User`, `ExecStart`, `Restart`, `After`, and `WantedBy` for httpd in `/root/httpd-unit-report.txt`.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `systemctl status`, `systemctl is-active`, `systemctl is-enabled`, `systemctl show`, `ss -lntup`, and relevant journal messages.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 10

### Task List

- Diagnose an instructor-created failure using unit status and journal records, correct only the faulty setting, reset failed state if needed, and prove a clean start.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `systemctl status`, `systemctl is-active`, `systemctl is-enabled`, `systemctl show`, `ss -lntup`, and relevant journal messages.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.
