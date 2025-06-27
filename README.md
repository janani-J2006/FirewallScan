# FirewallScan
#  Task: Setup and Use a Firewall on Linux (UFW)

This repository contains my work for the firewall configuration task. The objective was to configure UFW on a Linux system (Kali Linux), block inbound traffic on port 23 (Telnet), test the rule, and then restore the original firewall state.

---

##  Steps Performed

1. **Checked existing firewall rules:**
   - Used `sudo ufw status numbered` and `sudo ufw status verbose` to list the active rules.

2. **Enabled UFW (if not already active):**
   - Verified that UFW was active with default policy: deny incoming, allow outgoing.

3. **Added a rule to block port 23 (Telnet):**
   - Command used:
     ```bash
     sudo ufw deny 23
     ```

4. **Allowed SSH (port 22) to ensure secure access:**
   - Command used:
     ```bash
     sudo ufw allow 22
     ```

5. **Verified the firewall rules after adding the block:**
   - Confirmed the DENY rule on port 23 was present.

6. **Tested the block rule:**
   - Attempted to connect to port 23 using:
     ```bash
     telnet localhost 23
     ```
   - The connection failed as expected, confirming the block was effective.

7. **Removed the block rule to restore the original state:**
   - Command used:
     ```bash
     sudo ufw delete deny 23
     ```

8. **Confirmed final firewall rules to ensure cleanup:**
   - Used `sudo ufw status numbered` to verify port 23 block was removed.

---

## Evidence

Screenshots of the following are included in the firewall folder:
- Initial firewall rules
- Rules after blocking port 23
- Telnet test showing connection refused
- Final rules after removing the block

---

##  Outcome

- Successfully configured and managed firewall rules on Linux using UFW.
- Demonstrated ability to block and unblock specific ports.
- Verified firewall behavior through testing.

