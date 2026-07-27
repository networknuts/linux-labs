# 📡 Linux Administration Task: Access Network-Attached Storage

## Task List

- Configure an **automounter indirect map** on `servera` with **exports from `controller`**.  
- Create the following configuration files:
  - Master map file: `/etc/auto.master.d/shares.autofs`  
  - Mapping file: `/etc/auto.shares`  

- Use `/remote` as the **main mount point** on `servera`.  
- Reboot `servera` to verify that the **`autofs` service starts automatically**.

---

# Additional Network-Attached Storage Exercises

## Lab Environment and Rules

- Complete these exercises on servera as the client and controller as the NFS server.
- Work as root for configuration and student for access tests where appropriate.
- Confirm the exported path and server name before creating a client mount.
- Do not change exports on controller unless an exercise explicitly requires server-side work.
- Validate persistent mount syntax before rebooting and use a short timeout for troubleshooting tests.
- Persistent mounts and automounter maps must work after reboot; autofs paths must remain unmounted until accessed.

## Exercise 1

### Task List

- Query controller for exported paths and save the server, export names, and access information in `/root/controller-exports.txt` on servera.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `showmount -e`, `mount`, `findmnt`, `systemctl status autofs`, and creation and reading of a test file where export permissions allow.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 2

### Task List

- Mount the instructor-provided export temporarily at `/mnt/shared`, confirm its filesystem type is NFS, create a test file if permitted, and unmount it cleanly.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `showmount -e`, `mount`, `findmnt`, `systemctl status autofs`, and creation and reading of a test file where export permissions allow.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 3

### Task List

- Create an UUID-independent `/etc/fstab` NFS entry for the provided export at `/mnt/shared`, include `_netdev`, validate with `mount -a`, and verify after reboot.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `showmount -e`, `mount`, `findmnt`, `systemctl status autofs`, and creation and reading of a test file where export permissions allow.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 4

### Task List

- Add `x-systemd.automount` and `_netdev` for the NFS mount, reboot, confirm no active NFS mount before access, then access the path and confirm it mounts.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `showmount -e`, `mount`, `findmnt`, `systemctl status autofs`, and creation and reading of a test file where export permissions allow.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 5

### Task List

- Create master map `/etc/auto.master.d/shares.autofs` and map `/etc/auto.shares`; use `/remote` as the indirect-map root and mount the provided export through one key.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `showmount -e`, `mount`, `findmnt`, `systemctl status autofs`, and creation and reading of a test file where export permissions allow.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 6

### Task List

- Add keys `documents` and `software` to `/etc/auto.shares`, map each to its matching controller export, reload autofs, and access both paths independently.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `showmount -e`, `mount`, `findmnt`, `systemctl status autofs`, and creation and reading of a test file where export permissions allow.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 7

### Task List

- Create `/etc/auto.direct`, register it with `/-`, map `/mnt/direct-share` to the provided export, and verify on-demand mounting.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `showmount -e`, `mount`, `findmnt`, `systemctl status autofs`, and creation and reading of a test file where export permissions allow.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 8

### Task List

- Create wildcard key `*` below `/remote/home` so an accessed username maps to the matching exported home directory on controller.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `showmount -e`, `mount`, `findmnt`, `systemctl status autofs`, and creation and reading of a test file where export permissions allow.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 9

### Task List

- Set an automounter idle timeout of 60 seconds, access a mapped path, wait until it expires, and prove that a later access mounts it again.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `showmount -e`, `mount`, `findmnt`, `systemctl status autofs`, and creation and reading of a test file where export permissions allow.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 10

### Task List

- Enable autofs, reboot servera, prove the service is active, confirm mapped exports are initially unmounted, and access each configured key successfully.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `showmount -e`, `mount`, `findmnt`, `systemctl status autofs`, and creation and reading of a test file where export permissions allow.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.
