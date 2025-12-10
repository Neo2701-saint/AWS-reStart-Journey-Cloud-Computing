# __**Elastic Block Store (EBS) Lifecycle & Disaster Recovery**__

**Task 1: Storage Provisioning & Attachment**

By allocating persistent block storage to a compute instance.

EBS volumes are Availability Zone (AZ) locked. To attach an EBS volume 
to an EC2 instance, both resources must reside in the same physical 
Availability Zone (e.g., if the instance is in us-east-1a, the volume 
must also be in us-east-1a). This strict co-location requirement 
ensures the low-latency, high-bandwidth network connectivity necessary 
for reliable block storage performance.


__**I created a General Purpose SSD (gp2) EBS volume within the same Availability Zone as my EC2 instance and 
attaching the volume to the running Linux instance as a secondary block device ( /dev/sdb ).**__

<img width="754" height="290" alt="image" src="https://github.com/user-attachments/assets/7199d7d4-9203-4d36-8be9-5a73730cad3f" />
<img width="753" height="294" alt="image" src="https://github.com/user-attachments/assets/62857f88-32dc-4dcc-b022-4b6b41547352" />
<img width="751" height="260" alt="image" src="https://github.com/user-attachments/assets/11dbc557-d4ec-4980-b0a9-e191b3d8cc6e" />
<img width="763" height="238" alt="image" src="https://github.com/user-attachments/assets/532dc70a-a9d2-4135-92e1-f994bb1a9a99" />
<img width="758" height="295" alt="image" src="https://github.com/user-attachments/assets/70bf1a8d-68db-4115-88c6-bef8b2550df9" />

___

__**I verified the attachment via the AWS Console and the Linux terminal.**__
<img width="770" height="305" alt="image" src="https://github.com/user-attachments/assets/86fe2b26-206b-4af7-84f8-af69ef65c4ca" />

___

__**Task 2: File System Configuration & Mounting**__

To prepare the raw block storage for data operations.

A raw EBS volume requires a file system initialization (formatting) to 
function as a data store. Manual mounting is non-persistent; therefore, 
modifying the /etc/fstab configuration is critical to ensure the volume 
is automatically remounted upon system restart.

__**What I did:**__

- The volume was formatted with the ext3 file system using mkfs.
- A mount point, /mnt/data-store, was created and the volume was mounted.
- Persistence across reboots was configured by updating /etc/fstab.
- Test data (file.txt) was generated to simulate the production workload.

<img width="534" height="486" alt="image" src="https://github.com/user-attachments/assets/40d3d06c-0012-4cd6-8b6e-f37a54b85f8c" />

___

**Task 3: Backup Strategy**

To create a point-in-time backup for data durability.

EBS Snapshots are incremental backups of EBS volumes, stored securely 
in Amazon S3. They capture a volume's point-in-time state, providing 
crucial defense against data loss from events like accidental deletion or ransomware.

**I initiated a snapshot of the primary volume containing the test data and 
once the snapshot was secure, I intentionally deleted the file.txt 
from the primary volume to simulate data loss.**

<img width="757" height="299" alt="image" src="https://github.com/user-attachments/assets/861f7541-c4a5-48e4-ad04-583c37bd3061" />
<img width="753" height="179" alt="image" src="https://github.com/user-attachments/assets/1d566042-c818-447f-8e1f-56c956a16dd0" />
<img width="275" height="34" alt="image" src="https://github.com/user-attachments/assets/7b3243a4-0c36-44e7-8ba2-3d50bdf520a8" />


___

**Task 4: Disaster Recovery & Restoration**

To restore operations by recovering data from the snapshot.

To restore data, I must hydrate a new EBS volume from that snapshot. 
This new volume is an exact replica of the original drive at the exact 
second the snapshot was taken.

- I created a new EBS volume (Restored Volume) from the snapshot and 
- Attached the new volume to the instance as /dev/sdc.
- Mounted the restored volume to a new directory /mnt/data-store2.
- This allows for a successfully accessed file.txt on the restored drive.

<img width="759" height="298" alt="image" src="https://github.com/user-attachments/assets/b09d234c-3e3f-4ee0-9fd7-7c7c4c0ea9df" />
<img width="769" height="297" alt="image" src="https://github.com/user-attachments/assets/9d035a4f-1414-4852-aa26-9e340f858984" />
<img width="342" height="36" alt="image" src="https://github.com/user-attachments/assets/7b13d43a-5bd4-4861-9985-78d57ec09607" />
<img width="761" height="162" alt="image" src="https://github.com/user-attachments/assets/5ebb8733-3f90-4916-b152-459ccc5aadca" />
<img width="717" height="243" alt="image" src="https://github.com/user-attachments/assets/21e2bf1b-57b3-4377-9e64-2bf739c09164" />

___

# __**What I learned**__

Managed the end-to-end AWS Block Storage lifecycle, from provisioning 
and Linux file system configuration to implementing a successful EBS 
Snapshot-based Disaster Recovery (DR) workflow for guaranteed point-in-time data restoration.

