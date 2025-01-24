# Azure VM Backup and Restore for Disaster Recovery

![image](https://github.com/user-attachments/assets/5e96d8e7-db6e-4489-a259-f185ee813626)
In this screenshot I am connected to `BackupRestore-Project-VM` via RDP and created some sample data to prepare for backup.

![image](https://github.com/user-attachments/assets/945bcc6f-2c3d-4a6f-aafb-d9fbfd55a19c)
Here I create a Recovery Services vault in Azure

![image](https://github.com/user-attachments/assets/780d26ff-0e43-4aea-9462-da1f9ed1e56d)
Here ive configured a backup for `BackupRestore-Project-VM` with a newly created policy:

  - Backup frequency:
Every 4 hour(s) starting 7:00 AM UTC for 4 Hour(s)
  - Instant restore:
Retain instant recovery snapshot(s) for 10 day(s)
  - Retention of daily backup point:
Retain backup taken every day for 30 Day(s)

<img width="1344" alt="image" src="https://github.com/user-attachments/assets/77d1f369-d1c8-4786-a701-8a7276744806" />
![image](https://github.com/user-attachments/assets/ce9248a2-63c6-4c3f-b0f6-86b070bd2e2d)
Here i run an on-demand backup for the `BackupRestore-Project-VM`

