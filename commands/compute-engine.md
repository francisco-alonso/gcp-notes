**Compute Engine** is Google Cloud's Infrastructure-as-a-Service (IaaS) offering, allowing users to create and manage virtual machines (VMs) on Google Cloud. It provides flexibility in machine types, networking, and storage.

### 1. List all VM instances
```sh
gcloud compute instances list
```
**Explanation:** Lists all VM instances across all zones. Use `--filter` to narrow down results.

**Options:**
- `--filter=expression` → Filters results based on conditions (e.g., `status:RUNNING`).
- `--limit=NUMBER` → Limits the number of results.
- `--format=FORMAT` → Outputs in different formats (e.g., `json`, `yaml`, `table`).

### 2. Create a new VM instance
```sh
gcloud compute instances create INSTANCE_NAME --zone=ZONE --machine-type=MACHINE_TYPE --image-project=IMAGE_PROJECT --image=IMAGE
```
**Explanation:** Creates a new VM instance with the specified zone, machine type, and OS image.

**Options:**
- `--zone=ZONE` → Specifies the zone (e.g., `us-central1-a`).
- `--machine-type=MACHINE_TYPE` → Defines the VM size (e.g., `n1-standard-1`).
- `--image=IMAGE` → Specifies the OS image (e.g., `debian-10`).
- `--image-project=IMAGE_PROJECT` → Defines the project hosting the image (e.g., `debian-cloud`).

### 3. Delete a VM instance
```sh
gcloud compute instances delete INSTANCE_NAME --zone=ZONE
```
**Explanation:** Deletes a specific VM instance from a zone.

**Options:**
- `--quiet` → Skips confirmation prompts.

### 4. Start a stopped VM instance
```sh
gcloud compute instances start INSTANCE_NAME --zone=ZONE
```
**Explanation:** Starts a VM instance that has been previously stopped.

**Options:**
- `--async` → Runs the operation asynchronously.

### 5. Stop a running VM instance
```sh
gcloud compute instances stop INSTANCE_NAME --zone=ZONE
```
**Explanation:** Stops a running instance.

**Options:**
- `--async` → Runs the operation asynchronously.

### 6. SSH into a VM instance
```sh
gcloud compute ssh INSTANCE_NAME --zone=ZONE
```
**Explanation:** Establishes an SSH connection to a VM.

**Options:**
- `--internal-ip` → Connects using internal IP.
- `--ssh-key-file=FILE` → Specifies an SSH key file.

### 7. List machine types available in a region
```sh
gcloud compute machine-types list --filter="zone:REGION"
```
**Explanation:** Lists available machine types for a specific region.

### 8. Create a snapshot of a disk
```sh
gcloud compute disks snapshot DISK_NAME --zone=ZONE --snapshot-names=SNAPSHOT_NAME
```
**Explanation:** Creates a snapshot of a specified disk.

### 9. List available images
```sh
gcloud compute images list
```
**Explanation:** Lists all available images for VM instances.

### 10. Resize a persistent disk
```sh
gcloud compute disks resize DISK_NAME --size=SIZE --zone=ZONE
```
**Explanation:** Resizes a persistent disk to the specified size.

### 11. List available zones
```sh
gcloud compute zones list
```
**Explanation:** Lists all available zones in Google Cloud.

### 12. Change the machine type of a VM
```sh
gcloud compute instances set-machine-type INSTANCE_NAME --machine-type=MACHINE_TYPE --zone=ZONE
```
**Explanation:** Changes the machine type of an existing VM.

### 13. List all firewall rules
```sh
gcloud compute firewall-rules list
```
**Explanation:** Lists all firewall rules in the project.

### 14. Create a new firewall rule
```sh
gcloud compute firewall-rules create RULE_NAME --allow=PROTOCOL:PORT --direction=DIRECTION
```
**Explanation:** Creates a new firewall rule allowing traffic for a specific protocol and port.

### 15. Delete a firewall rule
```sh
gcloud compute firewall-rules delete RULE_NAME
```
**Explanation:** Deletes a specified firewall rule.

---