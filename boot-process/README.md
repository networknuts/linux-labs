# 🔄 Linux Administration Task: Control the Boot Process

## Task List

- Change the default `systemd` target on the `servera` machine so that the system automatically starts in **graphical mode** after boot.  

- Reset the **lost `root` user password** on the `servera` machine to `ablerate`.

---

# Additional Boot Process Exercises

## Lab Environment and Rules

- Complete these exercises on servera.
- Work as root; boot-loader recovery work must be performed from the server console.
- Confirm that console access is available before changing boot behavior.
- Do not leave the system in rescue or emergency mode after completing an exercise.
- Before rebooting, validate `/etc/fstab` and any configuration changed during the exercise.
- When a default target, password, or boot-time configuration is changed, reboot servera and prove that the requested state persists.

## Exercise 1

### Task List

- Record both the configured default target and the target currently active; explain any difference in `/root/boot-target-report.txt`.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `systemctl get-default`, `systemctl is-system-running`, `systemctl list-dependencies`, `findmnt --verify`, and `journalctl -b`.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 2

### Task List

- Set `multi-user.target` as the default without changing the current running target, then inspect the default-target symbolic link.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `systemctl get-default`, `systemctl is-system-running`, `systemctl list-dependencies`, `findmnt --verify`, and `journalctl -b`.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 3

### Task List

- Isolate `graphical.target` without rebooting, confirm the target becomes active, and return the machine to `multi-user.target` before finishing.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `systemctl get-default`, `systemctl is-system-running`, `systemctl list-dependencies`, `findmnt --verify`, and `journalctl -b`.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 4

### Task List

- Set `graphical.target` as the default on servera and prove after reboot that the target was reached without failed units.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `systemctl get-default`, `systemctl is-system-running`, `systemctl list-dependencies`, `findmnt --verify`, and `journalctl -b`.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 5

### Task List

- Save the recursive dependency tree for `multi-user.target` in `/root/multi-user-dependencies.txt` and identify at least three service units it pulls in.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `systemctl get-default`, `systemctl is-system-running`, `systemctl list-dependencies`, `findmnt --verify`, and `journalctl -b`.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 6

### Task List

- Enter emergency mode once from the boot loader, mount the root filesystem read-write if required, then continue booting to the configured default target.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `systemctl get-default`, `systemctl is-system-running`, `systemctl list-dependencies`, `findmnt --verify`, and `journalctl -b`.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 7

### Task List

- Enter rescue mode once, record the active targets and mounted filesystems, and return to the normal default target without powering off.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `systemctl get-default`, `systemctl is-system-running`, `systemctl list-dependencies`, `findmnt --verify`, and `journalctl -b`.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 8

### Task List

- Use the boot-loader break procedure, reset root's password to `ablerate`, trigger SELinux relabeling when required, and prove a console login after reboot.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `systemctl get-default`, `systemctl is-system-running`, `systemctl list-dependencies`, `findmnt --verify`, and `journalctl -b`.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 9

### Task List

- Add an invalid instructor-provided test mount, recover to a maintenance shell, correct `/etc/fstab`, and boot normally with no mount-unit failure.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `systemctl get-default`, `systemctl is-system-running`, `systemctl list-dependencies`, `findmnt --verify`, and `journalctl -b`.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 10

### Task List

- Save priority error messages from the current boot in `/root/boot-errors.txt`; the final check must show a running system with zero failed units.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `systemctl get-default`, `systemctl is-system-running`, `systemctl list-dependencies`, `findmnt --verify`, and `journalctl -b`.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.
