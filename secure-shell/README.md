# 🔐 Linux Administration Task: Configure and Secure SSH

## Task List

1. From the controller machine, log in to the `servera` machine as the `root` user.  
2. Switch to the `production1` user on the `servera` machine.  
3. Generate passphrase-less SSH keys for the `production1` user on the `servera` machine.  
4. Send the public key of the SSH key pair to the `production1` user on the `serverb` machine.  
5. Verify that the `production1` user can successfully log in to the `serverb` machine using the SSH keys.  
6. Configure the `sshd` service on `serverb` to prevent users from logging in as the `root` user.

---

# Additional Secure Shell Exercises

## Lab Environment and Rules

- Complete these exercises on controller as the originating client, servera for key creation where stated, and serverb as the destination server.
- Work as the user named in each exercise; use root only for sshd configuration.
- Keep one confirmed administrative session open while testing changes to sshd.
- Validate daemon configuration before reloading it and do not disable password login until key authentication is proven.
- Protect private keys and apply restrictive permissions to `.ssh`, private keys, and `authorized_keys`.
- Client configuration, authorized keys, and sshd drop-in settings must remain effective after logout and reboot.

## Exercise 1

### Task List

- From controller connect to `root@servera`, then record remote hostname, current user, source address, and SSH protocol details in `/root/ssh-first-login.txt`.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `ssh -v`, `ssh-keygen`, `ls -ld`, `sshd -t`, `sshd -T`, `systemctl status sshd`, and both allowed and denied login attempts.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 2

### Task List

- As `production1` on servera create an Ed25519 key pair in the default location with no passphrase; do not overwrite an existing private key.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `ssh -v`, `ssh-keygen`, `ls -ld`, `sshd -t`, `sshd -T`, `systemctl status sshd`, and both allowed and denied login attempts.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 3

### Task List

- Install only the new public key for `production1` on serverb, preserve any existing authorized keys, and complete a login with no password prompt.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `ssh -v`, `ssh-keygen`, `ls -ld`, `sshd -t`, `sshd -T`, `systemctl status sshd`, and both allowed and denied login attempts.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 4

### Task List

- Set the `.ssh` directory to `0700`, private key to `0600`, public key to `0644`, and `authorized_keys` to `0600`; confirm key login still works.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `ssh -v`, `ssh-keygen`, `ls -ld`, `sshd -t`, `sshd -T`, `systemctl status sshd`, and both allowed and denied login attempts.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 5

### Task List

- Create a client alias `production-server` in `production1`'s SSH config pointing to serverb, using user `production1` and the correct identity file.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `ssh -v`, `ssh-keygen`, `ls -ld`, `sshd -t`, `sshd -T`, `systemctl status sshd`, and both allowed and denied login attempts.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 6

### Task List

- Create `/home/production1/transfer-test.txt` on servera, copy it securely to the same user's home on serverb, and compare SHA-256 checksums.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `ssh -v`, `ssh-keygen`, `ls -ld`, `sshd -t`, `sshd -T`, `systemctl status sshd`, and both allowed and denied login attempts.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 7

### Task List

- Synchronize `/home/production1/project/` from servera to `/home/production1/project-copy/` on serverb over SSH; a second run must transfer no unchanged files.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `ssh -v`, `ssh-keygen`, `ls -ld`, `sshd -t`, `sshd -T`, `systemctl status sshd`, and both allowed and denied login attempts.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 8

### Task List

- Create an sshd drop-in on serverb setting `PermitRootLogin no`, validate configuration, reload sshd, prove root is rejected, and prove production1 still connects.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `ssh -v`, `ssh-keygen`, `ls -ld`, `sshd -t`, `sshd -T`, `systemctl status sshd`, and both allowed and denied login attempts.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 9

### Task List

- Set `PasswordAuthentication no` in a serverb drop-in only after key login succeeds; test a key login and a forced password-only login from a second terminal.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `ssh -v`, `ssh-keygen`, `ls -ld`, `sshd -t`, `sshd -T`, `systemctl status sshd`, and both allowed and denied login attempts.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 10

### Task List

- Create group `sshusers`, add `production1`, restrict serverb SSH access to that group, and demonstrate an allowed production1 login and a denied instructor test-user login.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `ssh -v`, `ssh-keygen`, `ls -ld`, `sshd -t`, `sshd -T`, `systemctl status sshd`, and both allowed and denied login attempts.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.
