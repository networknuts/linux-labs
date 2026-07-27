# 📂 Linux Administration Task: Access Linux File Systems

## Task List

- List all files in the `/usr/bin` directory with a file size greater than 50 KB.  
- Store the search result of all files in the `/usr/share` directory that are greater than 50 MB and less than 100 MB in the `/mnt/freespace/search2.txt` file.

---

# Additional Linux Filesystem Exercises

## Lab Environment and Rules

- Complete these exercises on controller.
- Work as root unless the exercise explicitly tests access as another user.
- Search only the path named in the exercise and redirect large result sets to the requested output file.
- Do not follow or cross into other filesystems unless the exercise explicitly requires it.
- Do not modify, move, or delete files returned by a search-only exercise.
- Search results and created links must remain available at the requested paths until graded.

## Exercise 1

### Task List

- Search `/usr/bin` for regular files larger than 50 KiB, sort the absolute paths by name, and store the results in `/root/usr-bin-over-50k.txt`.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `find`, `stat`, `file`, `ls -li`, `df -hT`, `findmnt`, and line or file counts for saved results.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 2

### Task List

- Find regular files in `/usr/share` larger than 50 MiB but smaller than 100 MiB and write absolute paths to `/mnt/freespace/search2.txt`.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `find`, `stat`, `file`, `ls -li`, `df -hT`, `findmnt`, and line or file counts for saved results.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 3

### Task List

- Find files owned by `student` below `/home` without reporting permission errors; save absolute paths and a total count in `/root/student-files.txt`.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `find`, `stat`, `file`, `ls -li`, `df -hT`, `findmnt`, and line or file counts for saved results.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 4

### Task List

- Search the root filesystem for regular files whose mode is exactly `0777`, do not cross filesystem boundaries, and save errors separately from results.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `find`, `stat`, `file`, `ls -li`, `df -hT`, `findmnt`, and line or file counts for saved results.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 5

### Task List

- Find regular files below `/var/log` modified within the previous 24 hours and produce a long listing sorted by modification time.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `find`, `stat`, `file`, `ls -li`, `df -hT`, `findmnt`, and line or file counts for saved results.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 6

### Task List

- List empty regular files and empty directories below `/tmp` in separate output files without deleting either type.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `find`, `stat`, `file`, `ls -li`, `df -hT`, `findmnt`, and line or file counts for saved results.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 7

### Task List

- Create `/tmp/link-lab/source.txt`, one hard link, and one symbolic link; record inode, link count, size, and behavior after renaming the source.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `find`, `stat`, `file`, `ls -li`, `df -hT`, `findmnt`, and line or file counts for saved results.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 8

### Task List

- Create `/root/filesystem-report.txt` showing source device, filesystem type, total size, available space, and mount options for `/`, `/boot`, and `/home` when separate.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `find`, `stat`, `file`, `ls -li`, `df -hT`, `findmnt`, and line or file counts for saved results.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 9

### Task List

- Investigate `ls` with `which`, `whereis`, and shell `type`; save the output and explain aliases, shell built-ins, and executable paths in two or three sentences.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `find`, `stat`, `file`, `ls -li`, `df -hT`, `findmnt`, and line or file counts for saved results.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 10

### Task List

- Copy every `.conf` regular file below `/etc` into `/root/conf-backup` while preserving paths relative to `/etc`; do not flatten duplicate filenames.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `find`, `stat`, `file`, `ls -li`, `df -hT`, `findmnt`, and line or file counts for saved results.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.
