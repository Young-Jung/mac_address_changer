Media Access Control Address Changer

- using subprocess module to execute system commands  
  import subprocess  
  subprocess.call("COMMAND", shell=True) - execute the command through the shell. It can be a security hazard, especially if you're passing user input to the command. It can lead to shell injection vulnerabilities. 
- using optparse module to parse command line options  
  import optparse  
- using Regular Expressions Ref. https://pythex.org/  
  import re  

python3 mac_changer.py -i eth0 -m 00:11:22:33:44:24

Why change the MAC address?
1. Increase anonymity.
2. Impersonate other devices.
3. Bypass filters.

You can change MAC address using ifconfig:

~# ifconfig eth0 down  -- disable interface  
~# ifconfig eth0 hw ether 00:11:22:33:44:55  -- modify interface  
~# ifconfig eth0 up  -- enable interface  
