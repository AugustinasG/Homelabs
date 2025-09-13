# Lab 04 – Local User + Group Management Lab

**Goal:**
Practice creating and managing local users, groups, and security policies on a standalone Windows 10 Pro machine.

---

**Environment:**

* Windows 10 Pro (Oracle VirtualBox)


---

**Steps to Reproduce:**

1. Created local users (Three accounts = Helpdesk1, Tech1, Supervisor1)
2. Created Helpdesk group and Supervisos Group. Put Helpdesk1 and Tech1 into Helpdesk, Supervisor1 into the Supervisors group. Added Supervisor1 to the Administrators group.
3. Applied Local security policies. Set the Minimum password length to 8, the maximum password age to 30 days, account lockout after 3 invalid attempts, and lockout duration set to 30 minutes.
4. Entered the wrong password 3 times with Helpdesk1 and got locked out. Logged in with supervisor1 and checked the Administrator status.



**Result:**

Three local user accounts created.
Users were sorted into groups.
Local security policies were applied.
Helpdesk1 got locked out.
Supervisor1 had administrator status.


---

**What I Learned:**

Creation of different local users. Applying different password policies and managing users.

---

**Screenshots:**
![Share-permissions](./screenshots/Share-permissions.png)
![ntfs-permissions](./screenshots/ntfs-permissions.png)
![alice-shares](./screenshots/alice-shares.png)
![Bob-shares](./screenshots/Bob-shares.png)
![mapped-drive](./screenshots/mapped-drive.png)
![alice-mapped](./screenshots/alice-mapped.png)
![bob-mapped](./screenshots/bob-mapped.png)





