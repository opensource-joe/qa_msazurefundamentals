# Zero Trust and Defense in Depth on Azure

## Zero Trust
- Don't trust anyone either inside or outside your perimeter.
- MS architecture principles:
    - Verify explicitly - verify based on all relevant user data points - userID and PW, conditional access by device and location, identity protection, and privileged identity management.
    - Use "lease privilege" access - only grant bare minimum access to a user who needs to do a task. Use JIT access for management access.
    - Assume breach - assume network and identity is breached. Known as minimizing the blast radius. Can run threat detection services and ensure all network traffic is encrypted. 

## Defense in Depth
- Confidentiality - only authorized users can access data.
- Integrity - data has not been altered by malicious users.
- Availability - authorized users can access data.
- Limit attack to layers - MS references seven:
    - Physical Security - MS maintains physical security at its datacenters.
    - Identity and Access Management - provided by Azure Active Directory and role-based access control. Examples are Conditional Access and Identity Protection.
    - Perimeter Security - Example is Azure DDOS.
    - Network Security - Example are security groups which are firewalls for networks.
    - Compute Security - Make sure OSs are regularly patched. Most Azure compute services regularly patch their operating system. Is using VMs, you must patch their operating systems manually.
    - Application Security - Ensure developers are writing applications in a secure manner. 
    - Data Security - Usually what attackers are trying to access. Azure offers a variety of data security features including encryption, advanced threat protection in Azure SQL database.

- Some layers are MS responsibility like Physical Security and others are personal security like Compute and Application Security.
