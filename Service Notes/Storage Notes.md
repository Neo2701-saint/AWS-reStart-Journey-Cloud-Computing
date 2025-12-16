# **Cloud Computing Storage Services Notes**

Cloud storage is the ability to store data on remote servers accessible over the internet, managed and maintained by a cloud service provider (CSP). It is a foundational service in cloud computing, offering scalability, durability, and cost-efficiency.

---

1. **The Three Main Storage Types**

Cloud storage is fundamentally categorized by how the data is organized, accessed, and used. The three main types are Object, Block, and File storage.

**Feature,	Object Storage (Unstructured Data),	Block Storage (Structured Data) and	File Storage (Shared Data)**

- **Data Organization**:	Flat structure data stored as discrete objects in buckets (no hierarchy).	
  -      Data split into fixed-size blocks; managed by the OS file system.
    -          Hierarchical structure of files and folders (familiar NAS/shared drive).
- **Access Method**:	API (HTTP/S) or URL. Ideal for web apps.
  -     Virtual disk that mounts to a single VM.
    -         Standard file-sharing protocols (NFS/SMB).
- **Scalability**:	Virtually unlimited (Exabytes). Highly scalable.
  -     Limited by the maximum size of a virtual disk (Petabytes).
    -       Limited by system design, but shareable across many VMs.
- **Performance**:	High throughput, suitable for large reads. Latency is higher than block.
  -     Lowest latency, highest IOPS (Input/Output Operations per Second).
    -       Moderate latency; performance can degrade with high concurrency.
- **Primary Use Cases**:	Data Lakes, Media files, Backups, Static Website Hosting, Archive.
  -     OS boot volumes for VMs, Databases (SQL/NoSQL), Transactional apps.
    -       Home directories, Collaborative shared drives, Lift-and-shift of file servers.
- **Major CSP Services**:	AWS S3, Azure Blob Storage.
  -     GCP Cloud Storage	AWS EBS, Azure Managed Disks.
    -       GCP Persistent Disk	AWS EFS/FSx, Azure Files/NetApp Files, GCP Filestore

---

2. **Deep Dive into Object Storage**

Object storage is the most flexible and scalable type of storage, designed for unstructured data.

_Key Features:_

 - **Durability**: CSPs typically promise 99.999999999% (11 nines) durability by replicating data across multiple devices and Availability Zones (AZs).

 - **Metadata**: Each object includes descriptive metadata, which can be customized (e.g., capture location, camera type) for enhanced search and management.

 - **Storage Classes/Tiers**: Designed to optimize cost based on access frequency and retrieval time.

**Tier Name (Generic), Access Frequency, Cost Model and Use Case**

- **Hot/Standard**:	Frequent access (daily/weekly)
  -     Higher storage cost, low/free retrieval
    -     Active data, production workloads
- **Cool/Infrequent Access (IA)**:	Infrequent access (monthly/quarterly)
  -     Lower storage cost, higher retrieval cost
    -     Backups, Disaster Recovery, Analytics
- **Archive/Deep Archive**:	Rare access (yearly/never)
  -     Lowest storage cost, significant retrieval time/cost
    -     Regulatory archives, long-term retention

_Key Capabilities:_

  - **Versioning**: Automatically keeps multiple versions of an object, protecting against accidental deletion or overwrite.

  - **Lifecycle Policies**: Rules to automatically transition objects between storage classes (e.g., move to Cool after 30 days) or permanently delete them, optimizing cost.

  -  **Replication**: Replicate objects to other regions for disaster recovery and compliance.

---

3. **Deep Dive into Block Storage**

Block storage is used primarily as the root disk/drive for compute instances (VMs).

- **Attachment:** Must be explicitly attached to a single compute instance, appearing as a local hard drive.

- **Performance**: Performance is measured in IOPS (Input/Output Operations Per Second) and throughput. CSPs offer different disk types (SSD-backed for high IOPS/low latency; HDD-backed for lower performance/lower cost).

- **Persistence**:

    - **Ephemeral/Instance Store**: Local disk storage that exists only for the life of the instance. Data is lost when the instance terminates.

    - **Persistent/Volume Storage** Network-attached storage that persists even after the VM is terminated. This is the standard for boot volumes and primary data storage.

---

4. **Backup, Migration, and Hybrid Services**

**Service Category,	Description and	CSP Examples**

- **Backup & Disaster Recovery**:	Managed services for automating snapshotting, backups, and replication of VMs, databases, and file systems.
  -     AWS Backup, Azure Backup, GCP Backup
- **Data Migration**:	Tools and appliances for transferring massive amounts of data from on-premises to the cloud (e.g., petabyte-scale data).
  -     AWS Snow Family, Azure Data Box, GCP Transfer Appliance/Service
- **Hybrid Cloud**:	Gateways that allow on-premises systems to use cloud storage as a local drive or tape library.
  -     AWS Storage Gateway, Azure StorSimple, GCP Storage Gateway



