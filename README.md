Remote Desktop Protocol (RDP) is a frequent target for brute-force and credential-stuffing attacks, especially on internet-facing Windows systems. 
This project demonstrates how to detect, investigate, and respond to RDP brute-force activity using Microsoft Sentinel.

I will be using my own lab, which is set up in Microsoft Azure with Microsoft Sentinel installed. I have created a rule in Sentinel to detect RDP brute-force alerts. Will remote login to a VM that Sentinel monitors. 
Will attempt an rdp brute force attempt to generate the alert in Sentinel. 

Objective
1. Trigger the brute force alert in Sentinel by logging into a VM
2. Identify and investigate the trigger alert in Sentiel
3. Document investigation

Tools & Technologies
1. RDP into VM
2. Windows Security Events
3. Microsoft Defender analytics and alerts page
