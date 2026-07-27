# 🧱 Linux Administration Task: Manage Storage Stack

## Task List

- Create a new **logical volume** with the following specifications:
  - Name: `database`  
  - Volume Group: `datastore`  
  - Size: **50 extents**  
  - Extent size for the `datastore` volume group should be set to **16 MiB**  

- Format the logical volume with an **ext3** filesystem.  
- Configure it to be **automatically mounted** under `/mnt/database` at **system boot**.  

- Resize the `database` logical volume so that its size is **approximately 900 MB**.  
  - Note: Only sizes between **870 MB and 890 MB** are accepted.

---

# Additional Advanced Storage Exercises

## Lab Environment and Rules

- Complete these exercises on serverb, using only the unused block devices assigned by the instructor.
- Work as the root user.
- Record the output of `lsblk` before making changes and confirm every selected device is unused.
- Use UUIDs or other stable identifiers for persistent entries; do not rely on a device name when a stable identifier is available.
- Do not remove or reformat an existing filesystem, physical volume, or logical volume unless the exercise explicitly created it.
- Any mount or swap configuration requested by an exercise must be added to `/etc/fstab`, validated without errors, and tested after a reboot.

## Exercise 1

### Task List

- Save the initial device inventory in `/root/adv-storage-before.txt`; the report must show device size, type, filesystem, mount point, and any existing LVM membership.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `pvs`, `vgs`, `lvs`, `lsblk -f`, `findmnt`, and the relevant filesystem or swap status command.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 2

### Task List

- Use an instructor-designated unused device for `vgdata`; confirm the 8 MiB physical extent size and leave at least 1 GiB free for later exercises.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `pvs`, `vgs`, `lvs`, `lsblk -f`, `findmnt`, and the relevant filesystem or swap status command.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 3

### Task List

- Create mount point `/reports`, add an UUID-based `/etc/fstab` entry, set ownership to `root:root`, and confirm that the mounted filesystem reports approximately 600 MiB.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `pvs`, `vgs`, `lvs`, `lsblk -f`, `findmnt`, and the relevant filesystem or swap status command.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 4

### Task List

- Name the second logical volume `lvarchive`, format it as ext4, mount it at `/archive`, and prove from LVM output that exactly 75 extents were allocated.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `pvs`, `vgs`, `lvs`, `lsblk -f`, `findmnt`, and the relevant filesystem or swap status command.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 5

### Task List

- Increase `lvreports` from 600 MiB to approximately 900 MiB without unmounting it or losing a test file created before the resize.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `pvs`, `vgs`, `lvs`, `lsblk -f`, `findmnt`, and the relevant filesystem or swap status command.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 6

### Task List

- Grow `lvarchive` to a final size of 1 GiB; expand both the logical volume and ext4 filesystem, then confirm the new usable capacity.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `pvs`, `vgs`, `lvs`, `lsblk -f`, `findmnt`, and the relevant filesystem or swap status command.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 7

### Task List

- Name the swap logical volume `lvswap`, assign it a 256 MiB size, add it to `/etc/fstab` by UUID, and use priority 20.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `pvs`, `vgs`, `lvs`, `lsblk -f`, `findmnt`, and the relevant filesystem or swap status command.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 8

### Task List

- Add a second instructor-designated device to `vgdata`; record total and free volume-group capacity before and after the addition.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `pvs`, `vgs`, `lvs`, `lsblk -f`, `findmnt`, and the relevant filesystem or swap status command.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 9

### Task List

- Relocate every allocated extent from the second physical volume, remove that PV from `vgdata`, and confirm that all logical volumes remain available.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `pvs`, `vgs`, `lvs`, `lsblk -f`, `findmnt`, and the relevant filesystem or swap status command.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 10

### Task List

- Write the final storage report to `/root/adv-storage-final.txt` and include proof that both filesystems are mounted and swap is active after reboot.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `pvs`, `vgs`, `lvs`, `lsblk -f`, `findmnt`, and the relevant filesystem or swap status command.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.
