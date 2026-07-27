# 🧰 Linux Administration Task: Tune System Performance

## Task List

- Change the current tuning profile for the `serverb` machine to the `balanced` profile, a general non-specialized tuned profile.  
  - List the information for the `balanced` tuning profile when it is the current tuning profile.  

- Change the current tuning profile for the `server` machine to the **recommended profile** as suggested by the system.

---

# Additional System Performance Tuning Exercises

## Lab Environment and Rules

- Complete these exercises on serverb.
- Work as root.
- Record the original active and recommended tuned profiles before changing anything.
- Do not terminate or renice classroom processes unless an exercise explicitly instructs you to do so.
- Collect performance observations for a reasonable interval rather than relying on a single instantaneous sample.
- The selected tuned profile must remain active after reboot when persistence is part of the exercise.

## Exercise 1

### Task List

- Confirm the tuned package is installed and its service is enabled and active; save package version and service state in `/root/tuned-status.txt`.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `tuned-adm`, `systemctl status tuned`, `uptime`, `top` or `ps`, `free`, `vmstat`, and `/proc` data where appropriate.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 2

### Task List

- List all available profiles, preserve the marker showing the active profile, and save the complete output in `/root/tuned-profiles.txt`.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `tuned-adm`, `systemctl status tuned`, `uptime`, `top` or `ps`, `free`, `vmstat`, and `/proc` data where appropriate.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 3

### Task List

- Record the active profile with the dedicated tuned command and confirm the tuned daemon reports a running state.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `tuned-adm`, `systemctl status tuned`, `uptime`, `top` or `ps`, `free`, `vmstat`, and `/proc` data where appropriate.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 4

### Task List

- Record the system-recommended profile in `/root/recommended-profile.txt` and do not change the active profile during this exercise.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `tuned-adm`, `systemctl status tuned`, `uptime`, `top` or `ps`, `free`, `vmstat`, and `/proc` data where appropriate.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 5

### Task List

- Activate `balanced`, confirm it is current, and record the active profile before and after the change.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `tuned-adm`, `systemctl status tuned`, `uptime`, `top` or `ps`, `free`, `vmstat`, and `/proc` data where appropriate.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 6

### Task List

- Display the full description of `balanced`, save it to `/root/balanced-profile-info.txt`, and identify its intended workload in one sentence.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `tuned-adm`, `systemctl status tuned`, `uptime`, `top` or `ps`, `free`, `vmstat`, and `/proc` data where appropriate.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 7

### Task List

- Activate exactly the profile recommended by the system, reboot serverb, and prove the same profile is still active.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `tuned-adm`, `systemctl status tuned`, `uptime`, `top` or `ps`, `free`, `vmstat`, and `/proc` data where appropriate.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 8

### Task List

- Turn tuned management off with the supported command, record the resulting state, restart management, and restore the recommended profile.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `tuned-adm`, `systemctl status tuned`, `uptime`, `top` or `ps`, `free`, `vmstat`, and `/proc` data where appropriate.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 9

### Task List

- Collect hostname, timestamp, uptime, load averages, CPU summary, memory and swap usage, and five one-second vmstat samples in `/root/performance-report.txt`.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `tuned-adm`, `systemctl status tuned`, `uptime`, `top` or `ps`, `free`, `vmstat`, and `/proc` data where appropriate.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 10

### Task List

- Take a process snapshot sorted by CPU and another sorted by resident memory, identify the top non-kernel process in each, and do not terminate or change either process.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `tuned-adm`, `systemctl status tuned`, `uptime`, `top` or `ps`, `free`, `vmstat`, and `/proc` data where appropriate.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.
