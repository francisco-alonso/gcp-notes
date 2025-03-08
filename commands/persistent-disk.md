**Persistent Disk** is a block storage solution for Compute Engine and Kubernetes Engine, providing high performance and reliability.

### 1. List all persistent disks
```sh
gcloud compute disks list
```
**Explanation:** Lists all persistent disks in a project.

### 2. Create a new persistent disk
```sh
gcloud compute disks create DISK_NAME --size=SIZE --zone=ZONE --type=TYPE
```
**Explanation:** Creates a new persistent disk.

### 3. Delete a persistent disk
```sh
gcloud compute disks delete DISK_NAME --zone=ZONE
```
**Explanation:** Deletes a specified persistent disk.

### 4. Resize a persistent disk
```sh
gcloud compute disks resize DISK_NAME --size=NEW_SIZE --zone=ZONE
```
**Explanation:** Increases the size of a persistent disk.

### 5. Snapshot a persistent disk
```sh
gcloud compute disks snapshot DISK_NAME --zone=ZONE --snapshot-names=SNAPSHOT_NAME
```
**Explanation:** Creates a snapshot of a persistent disk.

### 6. List snapshots
```sh
gcloud compute snapshots list
```
**Explanation:** Lists all disk snapshots.

### 7. Delete a snapshot
```sh
gcloud compute snapshots delete SNAPSHOT_NAME
```
**Explanation:** Deletes a specified disk snapshot.

### 8. Attach a disk to a VM
```sh
gcloud compute instances attach-disk INSTANCE_NAME --disk=DISK_NAME --zone=ZONE
```
**Explanation:** Attaches a persistent disk to a VM.

### 9. Detach a disk from a VM
```sh
gcloud compute instances detach-disk INSTANCE_NAME --disk=DISK_NAME --zone=ZONE
```
**Explanation:** Detaches a persistent disk from a VM.

### 10. Change disk type
```sh
gcloud compute disks update DISK_NAME --type=TYPE --zone=ZONE
```
**Explanation:** Updates a persistent disk's type.

### 11. List disk types
```sh
gcloud compute disk-types list
```
**Explanation:** Lists all available disk types.

### 12. Move a disk to another zone
```sh
gcloud compute disks move DISK_NAME --destination-zone=NEW_ZONE --zone=ZONE
```
**Explanation:** Moves a persistent disk to a new zone.

### 13. Create an image from a disk
```sh
gcloud compute images create IMAGE_NAME --source-disk=DISK_NAME --source-disk-zone=ZONE
```
**Explanation:** Creates an image from a persistent disk.

### 14. List all images
```sh
gcloud compute images list
```
**Explanation:** Lists all available disk images.

### 15. Delete an image
```sh
gcloud compute images delete IMAGE_NAME
```
**Explanation:** Deletes a specified disk image.

---