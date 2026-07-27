# 🗄️ Linux Administration Task: Archive and Transfer Files

## Task List

- On `serverb`, synchronize the `/etc` directory tree from `servera` to the `/configsync` directory.  
- Create a `configfile-backup-servera.tar.gz` archive with the contents of the `/configsync` directory.  
- Securely copy the `/root/configfile-backup-servera.tar.gz` archive file from `serverb` to the `/home/student` directory on `controller`.  
- Extract the contents to the `/tmp/savedconfig/` directory.

---

# Additional Archiving and File Transfer Exercises

## Lab Environment and Rules

- Complete these exercises on controller unless an exercise explicitly names servera or serverb.
- Work as root, switching to `student` only when ownership or access must be tested as that user.
- Create destination directories before extracting and never extract an unfamiliar archive directly into `/`.
- Preserve source data; an archive or synchronization task must not delete source files.
- Use absolute paths and confirm the destination host and directory before transferring data.
- These exercises do not require reboot persistence unless the instructor explicitly adds that requirement.

## Exercise 1

### Task List

- The archive must be `/root/ssh-config.tar`, contain paths relative to `/`, and include all regular files and subdirectories below `/etc/ssh`.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `tar -t`, `ls -l`, `find`, `du`, `sha256sum`, and a dry-run or itemized `rsync` comparison where appropriate.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 2

### Task List

- Create `/root/etc-backup.tar.gz` with gzip compression; exclude transient lock files and confirm that `/etc/fstab` is present in the archive.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `tar -t`, `ls -l`, `find`, `du`, `sha256sum`, and a dry-run or itemized `rsync` comparison where appropriate.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 3

### Task List

- Create `/root/logs.tar.bz2` with bzip2 compression from `/var/log`; unreadable files must be reported, not silently omitted.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `tar -t`, `ls -l`, `find`, `du`, `sha256sum`, and a dry-run or itemized `rsync` comparison where appropriate.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 4

### Task List

- Save the complete member listing in `/root/archive-contents.txt` without extracting any file and include the archive's compression type and size.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `tar -t`, `ls -l`, `find`, `du`, `sha256sum`, and a dry-run or itemized `rsync` comparison where appropriate.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 5

### Task List

- Create an empty `/tmp/ssh-restore`, extract into it, and confirm that the restored hierarchy does not add an unexpected leading directory.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `tar -t`, `ls -l`, `find`, `du`, `sha256sum`, and a dry-run or itemized `rsync` comparison where appropriate.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 6

### Task List

- Extract only `etc/ssh/sshd_config` from the archive into `/tmp/single-file-restore`; no other archive member may be restored there.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `tar -t`, `ls -l`, `find`, `du`, `sha256sum`, and a dry-run or itemized `rsync` comparison where appropriate.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 7

### Task List

- Archive `/home` as `/root/home-backup.tar.gz`, exclude every file whose name ends in `.tmp`, and prove excluded files are absent from the listing.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `tar -t`, `ls -l`, `find`, `du`, `sha256sum`, and a dry-run or itemized `rsync` comparison where appropriate.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 8

### Task List

- Synchronize `servera:/etc/` to `/configsync/` on serverb over SSH, preserve metadata where permitted, and ensure a second run reports no unnecessary transfers.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `tar -t`, `ls -l`, `find`, `du`, `sha256sum`, and a dry-run or itemized `rsync` comparison where appropriate.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 9

### Task List

- Copy `/root/configfile-backup-servera.tar.gz` from serverb to `/home/student/` on controller and make the resulting file owned by `student:student`.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `tar -t`, `ls -l`, `find`, `du`, `sha256sum`, and a dry-run or itemized `rsync` comparison where appropriate.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 10

### Task List

- Create SHA-256 checksums on both source and destination, require an exact match, extract into `/tmp/savedconfig`, and compare the restored file count with the archive listing.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `tar -t`, `ls -l`, `find`, `du`, `sha256sum`, and a dry-run or itemized `rsync` comparison where appropriate.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.
