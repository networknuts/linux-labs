# 📦 Linux Administration Task: Install and Update Software Packages

## Task List

- Create a repository.  
- On `controller`, install the `rht-system` package.  
- Remove the `rht-system` package.  
- Install the `httpd` package.

---

# Additional Package Management Exercises

## Lab Environment and Rules

- Complete these exercises on controller.
- Work as root.
- Inspect enabled repositories and package dependencies before installing, updating, or removing software.
- Do not disable the repository that provides required classroom packages.
- Do not remove dependency packages unless the transaction preview shows that unrelated software will remain installed.
- Repository definitions must be stored below `/etc/yum.repos.d` and remain usable after a reboot.

## Exercise 1

### Task List

- Save enabled and disabled repository IDs, names, base URLs, and status in `/root/repository-report.txt`; identify which repository provides BaseOS packages.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `dnf repolist`, `dnf info`, `dnf provides`, `rpm -q`, `rpm -ql`, and `dnf history` as appropriate.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 2

### Task List

- Create `/etc/yum.repos.d/training.repo` using the instructor-provided URL, repository ID `training`, descriptive name `RHCSA Training`, enabled state, and the specified GPG policy.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `dnf repolist`, `dnf info`, `dnf provides`, `rpm -q`, `rpm -ql`, and `dnf history` as appropriate.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 3

### Task List

- Disable repository `training` persistently and enable it again; demonstrate its state with both a repository listing and a package metadata refresh.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `dnf repolist`, `dnf info`, `dnf provides`, `rpm -q`, `rpm -ql`, and `dnf history` as appropriate.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 4

### Task List

- Identify the installed or available package that provides `/usr/bin/semanage` and save both the query and exact package name in `/root/provider.txt`.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `dnf repolist`, `dnf info`, `dnf provides`, `rpm -q`, `rpm -ql`, and `dnf history` as appropriate.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 5

### Task List

- Show httpd package summary, version, architecture, repository, dependencies, and installed file list; save results in `/root/httpd-package-info.txt`.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `dnf repolist`, `dnf info`, `dnf provides`, `rpm -q`, `rpm -ql`, and `dnf history` as appropriate.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 6

### Task List

- Install `httpd` from an enabled repository, confirm the installed NEVRA, and verify `/usr/sbin/httpd` belongs to that package.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `dnf repolist`, `dnf info`, `dnf provides`, `rpm -q`, `rpm -ql`, and `dnf history` as appropriate.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 7

### Task List

- Download but do not install one instructor-named RPM into `/root/rpms`; inspect its name, version, release, architecture, summary, and required packages.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `dnf repolist`, `dnf info`, `dnf provides`, `rpm -q`, `rpm -ql`, and `dnf history` as appropriate.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 8

### Task List

- Check the downloaded RPM's digest and signature, identify the signing key, and save the verification output in `/root/rpm-verification.txt`.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `dnf repolist`, `dnf info`, `dnf provides`, `rpm -q`, `rpm -ql`, and `dnf history` as appropriate.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 9

### Task List

- Update one instructor-approved package, record the transaction ID, inspect transaction details, and undo only that transaction when DNF reports it is safe.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `dnf repolist`, `dnf info`, `dnf provides`, `rpm -q`, `rpm -ql`, and `dnf history` as appropriate.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 10

### Task List

- Preview removal of the training package, confirm no unrelated packages are selected, remove it, and verify both the package and its command are absent.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `dnf repolist`, `dnf info`, `dnf provides`, `rpm -q`, `rpm -ql`, and `dnf history` as appropriate.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.
