# 🔐 Permissions Task 1

## 📋 Instructions:

**Do the following as the user `root`:**

---

## 📁 Group & File Permission Tasks

### 🔹 1.1
Create the `/root/consultants` directory

### 🔹 1.2
Create a group named `consultants`

### 🔹 1.3
Change the group ownership of the `consultants` directory to `consultants`

### 🔹 1.4
Add write permission to the `consultants` group for the directory

### 🔹 1.5
Ensure that no one else except the owner and group can access the `consultants` directory

### 🔹 1.6
Create an empty file called `consultant1.txt` inside the `consultants` directory

### 🔹 1.7
Change the group ownership of `consultant1.txt` to the `wheel` group

### 🔹 1.8
Add the text **"Hello world"** to the `consultant1.txt` file

### 🔹 1.9
Make the `consultant1.txt` file world writeable

---

---

# Additional File Permission Exercises

## Lab Environment and Rules

- Complete these exercises on servera.
- Work as root, with access tests performed as the affected non-root users.
- Record original ownership, mode, and ACL information before modifying an existing path.
- Do not use mode `0777` as a shortcut unless the exercise explicitly requests it.
- Test directory permissions by creating, reading, renaming, and deleting files as the affected users.
- Ownership, modes, special bits, and filesystem ACLs must remain correct after logout and reboot.

## Exercise 1

### Task List

- Create group `consultants`, directory `/root/consultants`, ownership `root:consultants`, and mode `0770`; verify a group member can create a file and an unrelated user cannot enter.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `ls -ld`, `stat`, `namei -l`, `getfacl`, and an access test performed as the relevant user.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 2

### Task List

- Create `/root/consultants/project.txt`, set ownership to `root:consultants`, and apply mode `0640` using symbolic operands rather than an octal mode.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `ls -ld`, `stat`, `namei -l`, `getfacl`, and an access test performed as the relevant user.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 3

### Task List

- Change `/root/consultants/project.txt` from `0640` to `0664` with one octal-mode operation and verify the resulting user, group, and other bits.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `ls -ld`, `stat`, `namei -l`, `getfacl`, and an access test performed as the relevant user.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 4

### Task List

- Create `/srv/development` owned by `root:development` with the setgid bit; files created there by development members must inherit group `development`.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `ls -ld`, `stat`, `namei -l`, `getfacl`, and an access test performed as the relevant user.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 5

### Task List

- Create `/srv/dropbox` with the sticky bit and write access for all users; prove one user cannot delete a file owned by another user.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `ls -ld`, `stat`, `namei -l`, `getfacl`, and an access test performed as the relevant user.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 6

### Task List

- In a controlled root shell set umask `0077`, create one file and one directory, confirm modes `0600` and `0700`, then restore the previous umask.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `ls -ld`, `stat`, `namei -l`, `getfacl`, and an access test performed as the relevant user.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 7

### Task List

- Create `/srv/reports/quarterly.txt` with mode `0600`; grant `john` read-only ACL access without changing its owner, group, or base mode.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `ls -ld`, `stat`, `namei -l`, `getfacl`, and an access test performed as the relevant user.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 8

### Task List

- Apply a default ACL on `/srv/development` granting group `development` read, write, and directory traversal; verify inheritance on a new file and subdirectory.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `ls -ld`, `stat`, `namei -l`, `getfacl`, and an access test performed as the relevant user.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 9

### Task List

- Search only `/usr/bin` for regular files with any setuid bit, sort the paths into `/root/setuid-files.txt`, and record the result count.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `ls -ld`, `stat`, `namei -l`, `getfacl`, and an access test performed as the relevant user.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 10

### Task List

- Copy `/srv/development` to `/backup/development` while preserving ownership, timestamps, modes, extended ACLs, and setgid behavior; compare both trees.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `ls -ld`, `stat`, `namei -l`, `getfacl`, and an access test performed as the relevant user.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.
