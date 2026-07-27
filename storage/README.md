# 💽 Linux Administration Task: Manage Basic Storage

## Task List

- On the `controller` machine (as `root`):
  - Create a **1 GB MBR partition**.  
  - Identify its **UUID**.  
  - Format the partition with an **XFS** file system.  
  - Persistently mount it using its UUID to the `/mnt/freespace` directory.  

- On the `serverb` machine:
  - Use the **first unused disk** to create a **2 GB MBR backup partition**.  
    - A size between **1.8 GB and 2.2 GB** is acceptable.  
  - Configure the backup partition with an **XFS** file system.  
  - Persistently mount the partition to the `/backup` directory.  

- On the same disk:
  - Create **two 512 MB MBR partitions** named `swap1` and `swap2`.  
    - A size between **460 MB and 564 MB** is acceptable.  
  - Set both partitions as **swap** type.  
  - Initialize both partitions as **swap spaces** and configure them to **activate at boot**.  
  - Set the **`swap2`** partition to be **preferred** over the other.

---

# Additional Basic Storage Exercises

## Lab Environment and Rules

- Complete these exercises on controller or serverb exactly as named by the exercise.
- Work as root.
- Run `lsblk` and identify instructor-designated unused storage before changing a partition table.
- Never format a device that already contains mounted data, a filesystem, LVM metadata, or active swap.
- Back up `/etc/fstab` and validate every new entry before rebooting.
- Filesystems must be mounted by UUID and swap entries must activate with the requested priority after reboot.

## Exercise 1

### Task List

- Save device name, size, type, partition-table type, filesystem, UUID, and mount point for every block device in `/root/storage-inventory.txt` before changes.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `lsblk -f`, the partitioning tool's print output, `blkid`, `findmnt`, `df -hT`, `swapon --show`, and `findmnt --verify`.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 2

### Task List

- On controller use an instructor-designated unused disk, create a DOS/MBR table and one 1 GiB primary partition, and confirm the kernel sees the new partition.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `lsblk -f`, the partitioning tool's print output, `blkid`, `findmnt`, `df -hT`, `swapon --show`, and `findmnt --verify`.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 3

### Task List

- Format the new 1 GiB partition as XFS, create `/mnt/freespace`, mount it temporarily, create a test file, and confirm the filesystem type.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `lsblk -f`, the partitioning tool's print output, `blkid`, `findmnt`, `df -hT`, `swapon --show`, and `findmnt --verify`.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 4

### Task List

- Add a UUID-based `/etc/fstab` entry for `/mnt/freespace`, use appropriate defaults, validate the file, unmount, and remount through the entry.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `lsblk -f`, the partitioning tool's print output, `blkid`, `findmnt`, `df -hT`, `swapon --show`, and `findmnt --verify`.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 5

### Task List

- On serverb create a 2 GiB MBR partition on the first unused disk, format it XFS, mount it by UUID at `/backup`, and verify after reboot.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `lsblk -f`, the partitioning tool's print output, `blkid`, `findmnt`, `df -hT`, `swapon --show`, and `findmnt --verify`.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 6

### Task List

- Create a 750 MiB partition on an instructor-designated disk, format it ext4, mount it by UUID at `/mnt/archive`, and confirm read-write access.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `lsblk -f`, the partitioning tool's print output, `blkid`, `findmnt`, `df -hT`, `swapon --show`, and `findmnt --verify`.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 7

### Task List

- Create two 512 MiB MBR partitions named logically in your report as `swap1` and `swap2`, set Linux swap type, initialize both, and record their UUIDs.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `lsblk -f`, the partitioning tool's print output, `blkid`, `findmnt`, `df -hT`, `swapon --show`, and `findmnt --verify`.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 8

### Task List

- Add both swap UUIDs to `/etc/fstab`, set priority 10 for swap1 and 20 for swap2, activate them without reboot, and confirm ordering.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `lsblk -f`, the partitioning tool's print output, `blkid`, `findmnt`, `df -hT`, `swapon --show`, and `findmnt --verify`.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 9

### Task List

- Create a test partition with adjacent free space, place the instructor-specified filesystem on it, write a test file, extend the partition and filesystem, and prove the file survived.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `lsblk -f`, the partitioning tool's print output, `blkid`, `findmnt`, `df -hT`, `swapon --show`, and `findmnt --verify`.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.

## Exercise 10

### Task List

- Back up `/etc/fstab`, add one commented and one deliberately invalid training entry, detect the invalid line without rebooting, remove it, and finish with clean validation and `mount -a`.
- Meet every name, path, size, address, time, port, permission, or other value exactly as written. Do not substitute different values unless the instructor approves them.
- Limit changes to resources used by this exercise and leave unrelated system configuration unchanged.

### Completion Criteria

- Verify the result with `lsblk -f`, the partitioning tool's print output, `blkid`, `findmnt`, `df -hT`, `swapon --show`, and `findmnt --verify`.
- Demonstrate both the configured state and its practical effect; a configuration file alone is not sufficient evidence.
- Record the commands used and the relevant verification output for instructor review.
