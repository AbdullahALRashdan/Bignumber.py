# Bignumber.py
#Final Jordan Cybertalents
Zero - %00Byte

#!/usr/bin/python

import requests 

payload = hex(999)
url="http://ec2-35-164-4-176.us-west-2.compute.amazonaws.com/bignumber/?password="+payload[2:]
session = requests.Session()
res = session.get(url)
print res.text.split("<center><h1>")[1]
