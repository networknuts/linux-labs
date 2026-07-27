# ⏰ Linux Administration Task: Schedule Future Task

## Task List

- Pass the `date >> /home/student/myjob.txt` string as the input to the `at` command so that the job runs **three minutes from now**.  

- Schedule a **recurring job** as the `student` user that appends the current date and time to the `/home/student/my_first_cron_job.txt` file **every two minutes**, but only from **Monday to Friday** (not on Saturday or Sunday).  

- Remove **all the scheduled recurring jobs** for the `student` user.

---

# Additional Scheduled Task Exercises

## Lab Environment and Rules

- Complete these exercises on controller.
- Work as the user named in the exercise; use root only for system-wide schedules or access-control files.
- Use full command paths in scheduled jobs when command lookup could be ambiguous.
- Redirect output to the file named in the exercise so that job execution can be verified.
- Do not remove schedules belonging to users other than the user named in the exercise.
- Recurring schedules must remain installed until an exercise explicitly asks for their removal.

## Exercise 1

### Task List

- Submit exactly `date >> /home/student/at-job.txt` for execution three minutes from the current time and confirm a new timestamp appears after the job runs.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `atq`, `at -c`, `crontab -l`, the relevant file timestamps and contents, and journal entries for the scheduling service.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 2

### Task List

- Save the pending job list in `/home/student/at-queue.txt` and save the inspected body of one selected job in `/home/student/at-job-body.txt`.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `atq`, `at -c`, `crontab -l`, the relevant file timestamps and contents, and journal entries for the scheduling service.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 3

### Task List

- Schedule a harmless job at least ten minutes ahead, record its job ID, remove that ID, and prove it no longer appears in the queue.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `atq`, `at -c`, `crontab -l`, the relevant file timestamps and contents, and journal entries for the scheduling service.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 4

### Task List

- Schedule `logger -t rhcsa-at "tomorrow job executed"` for 17:30 tomorrow and verify that the requested calendar time is shown in the queue.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `atq`, `at -c`, `crontab -l`, the relevant file timestamps and contents, and journal entries for the scheduling service.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 5

### Task List

- Install a student crontab entry that appends `five-minute-run` and the date to `/home/student/five-minute-job.log` every five minutes.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `atq`, `at -c`, `crontab -l`, the relevant file timestamps and contents, and journal entries for the scheduling service.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 6

### Task List

- Append the date to `/home/student/my_first_cron_job.txt` every two minutes only Monday through Friday; the schedule must exclude Saturday and Sunday.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `atq`, `at -c`, `crontab -l`, the relevant file timestamps and contents, and journal entries for the scheduling service.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 7

### Task List

- Create a job that writes `weekly-maintenance` to `/home/student/weekly.log` at 02:15 every Sunday and confirm all five cron fields.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `atq`, `at -c`, `crontab -l`, the relevant file timestamps and contents, and journal entries for the scheduling service.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 8

### Task List

- Create `/etc/cron.d/training-report` to run `/usr/bin/uptime` as `student` at 06:00 daily; set file ownership and permissions accepted by crond.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `atq`, `at -c`, `crontab -l`, the relevant file timestamps and contents, and journal entries for the scheduling service.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 9

### Task List

- Permit `student` and deny the instructor-named test user access to `at`; demonstrate an accepted submission and a rejected submission.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `atq`, `at -c`, `crontab -l`, the relevant file timestamps and contents, and journal entries for the scheduling service.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 10

### Task List

- Remove the student's entire crontab, confirm `crontab -l` reports none, and leave system-wide schedules and other users' crontabs unchanged.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `atq`, `at -c`, `crontab -l`, the relevant file timestamps and contents, and journal entries for the scheduling service.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.
