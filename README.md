Task 4 – Firewall Configuration, Testing & Removal (UFW)

Objective:
The objective of this task is to configure and test the Uncomplicated Firewall (UFW) on Linux.  
This includes enabling the firewall, adding allow/deny rules, testing them, and restoring the original state.

---

Steps Performed:

1)Check Firewall Status:
  sudo ufw status

Step 1 – Status inactive(images/Step1.png)

---

2)Enable UFW:
  
  sudo ufw enable

[Step 2 – Firewall enabled](images/Step2.png)

---

3)Allow SSH (Port 22):

  sudo ufw allow 22/tcp

[Step 3 – SSH allowed](images/Step3.png)

---

4)Block Telnet (Port 23):

  sudo ufw deny 23/tcp

[Step 4 – Telnet blocked](images/Step4.png)

---

5)View All Rules:

  sudo ufw status verbose

[Step 5 – Rules list](images/Step5.png)

---

6)Test the Block:
  telnet localhost 23
  
[Step 6 – Telnet blocked test](images/Step6.png)

---

7)Remove the Telnet Block (Restore Original State):
  sudo ufw delete 2
  sudo ufw delete 3

[Step 7 – After deletion](images/Step7.1.png ; images/Step7.2.png)

---

Conclusion
- Successfully enabled and configured UFW.
- Added allow/deny rules for specific ports.
- Verified Telnet port block through testing.
- Restored firewall to its original state.


