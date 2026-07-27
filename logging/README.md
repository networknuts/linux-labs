# 📊 Linux Administration Task: Analyze and Store Logs

## Task List

1. View the recorded log events in the previous 30 minutes on the `serverb` machine.  
2. Create the `/etc/rsyslog.d/auth-errors.conf` file. Configure the `rsyslog` service to write authentication and security messages to the `/var/log/auth-errors` file using the `authpriv` facility and the `alert` priority.

---

# Additional Logging Exercises

## Lab Environment and Rules

- Complete these exercises on serverb.
- Work as root.
- Create service configuration as a separate drop-in file rather than editing an unrelated vendor file.
- Run a syntax or configuration check when the service provides one before restarting it.
- Generate a controlled test event with `logger` instead of waiting for a real security event.
- Rsyslog, journal-storage, and log-rotation changes must survive a reboot and continue writing to the requested destination.

## Exercise 1

### Task List

- Save all serverb journal events from the previous 30 minutes in `/root/journal-last-30-minutes.txt`, including timestamps and without truncating long messages.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `journalctl`, `logger`, `systemctl status rsyslog`, file ownership and permissions, and the contents of the requested log.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 2

### Task List

- Save messages from only the current boot in `/root/current-boot.log` and record the current boot ID at the top of the report.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `journalctl`, `logger`, `systemctl status rsyslog`, file ownership and permissions, and the contents of the requested log.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 3

### Task List

- Display priority warning through emergency for the current boot, save the output to `/root/boot-warnings.log`, and include at least one generated test warning.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `journalctl`, `logger`, `systemctl status rsyslog`, file ownership and permissions, and the contents of the requested log.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 4

### Task List

- Write sshd journal messages from the current boot to `/root/sshd-journal.log`; include unit metadata and both successful and failed authentication events if available.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `journalctl`, `logger`, `systemctl status rsyslog`, file ownership and permissions, and the contents of the requested log.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 5

### Task List

- Follow the journal in one terminal, generate `RHCSA live log test` with tag `rhcsa-lab` from another terminal, and capture the matching event in `/root/live-log-test.txt`.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `journalctl`, `logger`, `systemctl status rsyslog`, file ownership and permissions, and the contents of the requested log.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 6

### Task List

- Select an instructor-provided start and end time on the same day, query only that interval, and save the exact query times with the returned events.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `journalctl`, `logger`, `systemctl status rsyslog`, file ownership and permissions, and the contents of the requested log.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 7

### Task List

- Configure persistent journal storage below `/var/log/journal`, restart the journal service safely, reboot, and prove that events from the preceding boot remain queryable.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `journalctl`, `logger`, `systemctl status rsyslog`, file ownership and permissions, and the contents of the requested log.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 8

### Task List

- Create `/etc/rsyslog.d/training.conf` so `local5.notice` and higher priorities go to `/var/log/training.log`; set secure ownership and test with both notice and info messages.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `journalctl`, `logger`, `systemctl status rsyslog`, file ownership and permissions, and the contents of the requested log.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 9

### Task List

- Create `/etc/rsyslog.d/auth-errors.conf` so only `authpriv.alert` and higher messages go to `/var/log/auth-errors`; validate syntax, restart rsyslog, and generate a controlled matching event.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `journalctl`, `logger`, `systemctl status rsyslog`, file ownership and permissions, and the contents of the requested log.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 10

### Task List

- Create `/etc/logrotate.d/training` for `/var/log/training.log`; rotate weekly, keep four compressed archives, create a new secure log, and demonstrate one forced rotation.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `journalctl`, `logger`, `systemctl status rsyslog`, file ownership and permissions, and the contents of the requested log.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.
