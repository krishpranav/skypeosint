# skypeosint
 This tool allows you to retrieve the Skype ID from an e-mail address but also the LAN IP from the Skype ID. More to come in the next few days. Feel free if you also want to contribute

[![forthebadge](https://forthebadge.com/images/badges/made-with-python.svg)](https://forthebadge.com)

# Installation
```
git clone https://github.com/krishpranav/skypeosint
cd skypeosint
chmod +x *
python -m pip install -r requirements.txt
python skypeosint.py
```

# Example
```python
from SkypeOsintAPI import *

api = SkypeOSINTAPI(True)
res = api.email_to_skype_id('username@gmail.com')

if res:
    print "Username(s) found: {0}".format(res)
    for username in res:
        print api.skype_id_to_lan_ip(username)
        
```
