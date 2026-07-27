# 🐧 Linux Training Lab: User, Group & Password Management

Welcome to your Linux system administration lab. Complete the following tasks to practice group management, user management, password policies, and advanced account handling.

---

## 📁 1. Group Management Tasks

### 🔹 1.1
Create a group named `operations`

### 🔹 1.2
Create a group named `development` with the GID of `1008`

---

## 👤 2. User Management Tasks

### 🔹 2.1
Create a user named `john` with primary group as `operations`

### 🔹 2.2
Create a user named `jane` with secondary group as `development`

### 🔹 2.3
Create a user named `tom` with UID `1010` and secondary group as `operations`

### 🔹 2.4
Assign all three users the password `p@55w0rd`

---

## 🔒 3. Password Management Tasks

### 🔹 3.1
Do NOT allow the users to change their password for 7 days after a password change

### 🔹 3.2
Set the maximum age of the password to 30 days for the above-created users

### 🔹 3.3
On the 20th day, the users should start receiving a warning to change their password

### 🔹 3.4
Set an inactivity period of 14 days for the above users

---

## 🛠️ 4. Advanced User Management

### 🔹 4.1
Lock the `john` user immediately

### 🔹 4.2
Lock the `jane` user on **1st July 2026**

### 🔹 4.3
The user `tom` is under investigation, thus change the user's shell to `nologin`

---

---

# Additional User and Group Management Exercises

## Lab Environment and Rules

- Complete these exercises on servera.
- Work as root.
- Check existing usernames, UIDs, group names, and GIDs before creating accounts.
- Set passwords without exposing them in command history or process listings.
- Do not delete a user's home directory until its contents and ownership have been reviewed.
- Account, group, password-aging, expiry, and login-shell settings must remain correct after reboot.

## Exercise 1

### Task List

- Create group `operations` with the next available GID and group `development` with GID `1008`; fail safely if either name or GID already exists.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `id`, `getent passwd`, `getent group`, `passwd -S`, `chage -l`, home-directory ownership, and an actual login or denial test.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 2

### Task List

- Create user `john` with `operations` as the primary group, a normal home directory, Bash login shell, and no supplementary group unless required elsewhere.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `id`, `getent passwd`, `getent group`, `passwd -S`, `chage -l`, home-directory ownership, and an actual login or denial test.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 3

### Task List

- Create user `jane` with a normal private primary group and `development` as a supplementary group; verify membership through the account database.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `id`, `getent passwd`, `getent group`, `passwd -S`, `chage -l`, home-directory ownership, and an actual login or denial test.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 4

### Task List

- Create user `tom` with UID `1010`, a normal home directory, Bash shell, and `operations` as a supplementary group; confirm UID uniqueness before creation.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `id`, `getent passwd`, `getent group`, `passwd -S`, `chage -l`, home-directory ownership, and an actual login or denial test.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 5

### Task List

- Set the instructor-provided initial password without exposing it in shell history, force a change at first login, and verify password status for john, jane, and tom.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `id`, `getent passwd`, `getent group`, `passwd -S`, `chage -l`, home-directory ownership, and an actual login or denial test.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 6

### Task List

- For all three users set minimum password age 7 days, maximum age 30 days, warning period 10 days, and inactivity lock 14 days; compare each resulting policy.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `id`, `getent passwd`, `getent group`, `passwd -S`, `chage -l`, home-directory ownership, and an actual login or denial test.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 7

### Task List

- Lock john immediately, prove password authentication is disabled, unlock him, and prove the stored password-aging policy was not lost.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `id`, `getent passwd`, `getent group`, `passwd -S`, `chage -l`, home-directory ownership, and an actual login or denial test.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 8

### Task List

- Set jane's account expiry to July 1, 2026 in ISO format, display the stored date, and note that the account is already expired when testing after that date.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `id`, `getent passwd`, `getent group`, `passwd -S`, `chage -l`, home-directory ownership, and an actual login or denial test.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 9

### Task List

- Change tom's shell to `/sbin/nologin`, attempt an interactive login, capture the denial, and confirm that his UID, groups, home, and files remain unchanged.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `id`, `getent passwd`, `getent group`, `passwd -S`, `chage -l`, home-directory ownership, and an actual login or denial test.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 10

### Task List

- Create `projectuser` with UID `1050` and home `/srv/projectuser`, rename it to `archiveuser` while moving home to `/srv/archiveuser`, verify ownership, then remove the account and home after inspection.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `id`, `getent passwd`, `getent group`, `passwd -S`, `chage -l`, home-directory ownership, and an actual login or denial test.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.
