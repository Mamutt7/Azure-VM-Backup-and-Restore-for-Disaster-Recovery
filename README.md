# **Azure VM Backup and Restore for Disaster Recovery**

## **Project Overview**
This project demonstrates how to configure an Azure Virtual Machine (VM) backup and restore process for disaster recovery using Azure Recovery Services Vault. The steps include creating a Recovery Services Vault, configuring a backup policy, running an on-demand backup, simulating a disaster, and restoring the VM.

---

## **1. Preparing the VM for Backup**
![image](https://github.com/user-attachments/assets/5e96d8e7-db6e-4489-a259-f185ee813626)

In this step, I connected to the `BackupRestore-Project-VM` via RDP and created sample data to prepare for the backup.

---

## **2. Creating a Recovery Services Vault**
![image](https://github.com/user-attachments/assets/945bcc6f-2c3d-4a6f-aafb-d9fbfd55a19c)

I created a Recovery Services Vault in Azure to manage backups and restores for the VM.

---

## **3. Configuring Backup for the VM**
![image](https://github.com/user-attachments/assets/780d26ff-0e43-4aea-9462-da1f9ed1e56d)

The backup configuration for `BackupRestore-Project-VM` was completed with the following policy:
- **Backup frequency:** Every 4 hours starting at 7:00 AM UTC.
- **Instant restore retention:** 10 days.
- **Daily backup retention:** 30 days.

---

## **4. Running an On-Demand Backup**
![image](https://github.com/user-attachments/assets/ce9248a2-63c6-4c3f-b0f6-86b070bd2e2d)

I initiated an on-demand backup for `BackupRestore-Project-VM` to ensure data was captured before simulating a disaster.

---

## **5. Simulating a Disaster by Deleting the VM**
![image](https://github.com/user-attachments/assets/cdb743b0-4529-4246-94b7-4231fde4a337)

To simulate a disaster recovery scenario, I deleted the `BackupRestore-Project-VM` after confirming the backup was successful.

---

## **6. Restoring the Deleted VM**
![image](https://github.com/user-attachments/assets/ff3864b8-ef57-4d0a-8f4a-6a5ed2c7e801)

In the restore configuration, I:
- Selected the backup restore point.
- Created a staging location (`stagingbackupstorage1`) to resolve an issue where no staging location options were available initially.
- Configured the restored VM as `RestoredBackupRestoreVM`.

---

## **7. Backup and Restore Completion**
![image](https://github.com/user-attachments/assets/322f58fe-d771-48ac-960e-308f00866a43)
![image](https://github.com/user-attachments/assets/6e41f2fe-485b-4803-89c3-90c2b158844f)

The backup process was successfully completed, and the VM was restored. The restored VM includes all data and configurations from the backup.

---

## **Key Learnings**
1. Azure Recovery Services Vault simplifies backup and restore processes for VMs.
2. A staging location is required for restoring VMs when certain storage configurations are used.
3. Regular backups are essential for disaster recovery and maintaining business continuity.

---

This project demonstrates practical experience in managing Azure VM backups and restores. For questions or feedback, feel free to reach out.
