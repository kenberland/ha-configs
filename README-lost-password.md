```
docker exec -it home-assistant bash
bash-5.0# python
Python 3.7.4 (default, Oct 15 2019, 14:28:50)
[GCC 8.3.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> import bcrypt
>>> import base64
>>> password="foobar"
>>> hashed = bcrypt.hashpw(password.encode(), bcrypt.gensalt(rounds=12))
>>> hashed = base64.b64encode(hashed)
>>> print(hashed)
```

put that into `auth_provider.homeassistant`

