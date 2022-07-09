# Free SMS sender (Egyption numbers only)
this function will allow you to send free sms to any egyption number,i think this endpoint has no limits 😁.
```python
from urllib import response
import requests
def SendFreeSms(phone,message,debug=True):
    resp = requests.post("https://www.amanshops.com/AmanAPI/Installment/CreateOTP/"
        ,json={
  "MobileNumber": phone,
  "HashCode": message,
  "lang": "0"}).text
    if debug:
        print(resp)
    if "Success" in resp:
        return True
    else:return False
```
## Example
```python 
SendFreeSms("01xxxxxxxxx","""
اهلا بك 
رسالة من طارق تربو بواسطة امان
Welcome 
a message from tarek turbo by aman
""")
```
![sms](https://user-images.githubusercontent.com/74266531/178124124-ed0c6946-598b-4557-96d9-1386237151c0.jpg)
