Media Access Control Address Changer

- using subprocess module to execute system commands
  import subprocess
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

~# ifconfig eth0 down
~# ifconfig eth hw ether 00:11:22:33:44:55
~# ifconfig eth0 up
