>Objective:

Demonstrate how to create, test, and remove inbound firewall rules on Windows to:
- Block Telnet traffic (Port 23)
- Allow SSH traffic (Port 22)
This task simulates controlling network access for security purposes.

>Tools Used:

- Windows Defender Firewall (Advanced Settings)
- Command Prompt
- Telnet Client (enabled via optionalfeatures)
- Nmap for verification

>Steps Performed:

1. Block Telnet (Port 23)
- Opened Windows Defender Firewall with Advanced Security (wf.msc)
- Went to Inbound Rules → New Rule
- Selected Port → TCP → Specific local port: 23
- Chose Block the connection
- Applied to Domain, Private, Public
- Named rule Block Telnet
- Verified the rule appears in inbound rules list

2. Test Block Telnet Rule
Ran the command:
telnet localhost 23
Result:
Connecting To localhost...Could not open connection to the host, on port 23: Connect failed
Confirms firewall is blocking Port 23.

3. Allow SSH (Port 22)
-- Created a new inbound rule:
- Port → TCP → Specific local port: 22
- Allow the connection
- Applied to Domain, Private, Public
- Named rule Allow SSH
-- Verified rule appears in inbound rules list.

4. Remove Block Telnet Rule (Optional)
- Right-clicked Block Telnet rule → Delete
- Confirmed it’s no longer in the list.

>Results & Observations:

- Successfully blocked Telnet (Port 23) and confirmed via Telnet test.
- Successfully created an allow rule for SSH (Port 22).
- Learned how to add, test, and remove firewall rules in Windows.

>Key Learnings:

- Inbound rules control what external traffic can enter your system.
- Blocking unused ports reduces attack surface.
- Allowing only necessary ports follows the principle of least privilege.
