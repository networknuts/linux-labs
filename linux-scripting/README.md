# ⚙️ Linux Administration Task: Improve Command-line Productivity

## Task List

- Create the `/home/student/bin/bash-lab` script file on the `controller` machine.  
  - The initial content should be the **shebang** interpreter directive.  

- Edit the newly created script file to include the following commands and outputs:

| Command                                     | Output Required                           |
|---------------------------------------------|--------------------------------------------|
| `echo "This is my first bash script"`       | Get all the output                         |
| `echo "#####################"`              | Get all the output                         |
| `echo "LIST BLOCK DEVICES"`                 | Get all the output                         |
| `lsblk`                                     | Get all the output                         |
| `echo "#####################"`              | Get all the output                         |
| `echo "FILESYSTEM FREE SPACE STATUS"`       | Get all the output                         |
| `df -h`                                     | Get all the output                         |
| `echo "#####################"`              | Get all the output                         |
| `lscpu`                                     | Get only the lines that start with "CPU"   |

- Save the required output into a file named `output.txt` inside the `/home/student` directory on the `controller` machine.  

- Execute the `/home/student/bin/bash-lab` script and review the output content on the `controller`.  

- Find all occurrences of the string `"ing"` in the `/usr/share/dic/words` file and copy the results into `/root/data`.

---

# Additional Bash Scripting Exercises

## Lab Environment and Rules

- Complete these exercises on controller.
- Work as student for files below `/home/student`; use root only when a destination requires root privileges.
- Begin each script with `#!/bin/bash`, make it executable, and avoid embedding passwords or other secrets.
- Quote variable expansions and validate every required argument before using it.
- Send normal output to standard output, errors to standard error, and return a nonzero status when a requested operation fails.
- Save scripts below `/home/student/bin` unless another path is specified, and leave them executable for grading.

## Exercise 1

### Task List

- Create `/home/student/bin/system-report`; print the original lab headings, full `lsblk` and `df -h` output, and only lines from `lscpu` that begin with `CPU`; redirect one complete run to `/home/student/output.txt`.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `bash -n`, `ls -l`, normal and failure-case executions, `$?`, and inspection of every requested output file.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 2

### Task List

- Create `/home/student/bin/greet`; accept exactly one name as `$1`, print `Hello, NAME`, and print `Usage: greet NAME` to standard error with exit status 2 when the argument is missing.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `bash -n`, `ls -l`, normal and failure-case executions, `$?`, and inspection of every requested output file.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 3

### Task List

- Create `/home/student/bin/path-type`; accept one path and report `regular file`, `directory`, `symbolic link`, or `not found`; test it with one example of every type.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `bash -n`, `ls -l`, normal and failure-case executions, `$?`, and inspection of every requested output file.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 4

### Task List

- Create `/home/student/user-list.txt` containing `root`, `student`, and `missinguser`; write a loop that checks the account database and prints `EXISTS` or `MISSING` beside each name.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `bash -n`, `ls -l`, normal and failure-case executions, `$?`, and inspection of every requested output file.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 5

### Task List

- Create `/home/student/bin/disk-warning`; process numeric usage from `df -P`, print only filesystems at or above 80 percent, and print `No filesystems above threshold` when none qualify.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `bash -n`, `ls -l`, normal and failure-case executions, `$?`, and inspection of every requested output file.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 6

### Task List

- Create `/home/student/bin/backup-dir`; require a readable source directory, write `NAME-YYYYMMDD-HHMMSS.tar.gz` below `/home/student/backups`, and refuse a nonexistent source.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `bash -n`, `ls -l`, normal and failure-case executions, `$?`, and inspection of every requested output file.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 7

### Task List

- Create `/home/student/bin/ssh-log-count`; accept a readable log path and print separate numeric totals for accepted and failed SSH authentication records without altering the log.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `bash -n`, `ls -l`, normal and failure-case executions, `$?`, and inspection of every requested output file.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 8

### Task List

- Create `/home/student/bin/service-control`; accept a service name and one action from `start`, `stop`, `restart`, or `status`; reject every other action with usage text and a nonzero status.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `bash -n`, `ls -l`, normal and failure-case executions, `$?`, and inspection of every requested output file.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 9

### Task List

- Write all lines containing lowercase `ing` from `/usr/share/dict/words` to `/root/data`, one matching source line per output line, and print the match count after a successful run.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `bash -n`, `ls -l`, normal and failure-case executions, `$?`, and inspection of every requested output file.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 10

### Task List

- Create `/home/student/bin/process-input`; require an input file and output file, reject identical paths, log errors to standard error, use distinct exit codes for missing arguments and unreadable input, and append a timestamped success message to `/home/student/script.log`.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `bash -n`, `ls -l`, normal and failure-case executions, `$?`, and inspection of every requested output file.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.
