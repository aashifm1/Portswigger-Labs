# Username enumeration via different responses

> Tool used: **Burp Intruder**

Given credentials dump:
- username.txt
- password.txt


## Login functionality 

- First i entered usual creds, wiener:peter --> response invalid username

> Request parameter: username=wiener&password=peter

- The webapp first check username, if it is correct then check for password

The WebApp Logic:

```bash
check_username():
  if username = actual_username:
  	check_password()
  else:
  	print("Invalid username")
    break

check_password():
	if password = actual_password:
		response(302_statuscode) 
	else:
		print("Invalid password")

check_username() 
```

When finding username:

> username: username=$$&password=wiener

When finnding password:

> password: username=autodiscover&password=$$

checks the length while invalid gives same response when bruteforce

<img width="800" height="563" alt="Screenshot 2026-04-09 184540" src="https://github.com/user-attachments/assets/5c1ef469-1b53-442b-a44d-bbb57e6adcde" />


## FInal correct credentials

```bash
username: autodiscover
password: 123123
```

> **Boom lab solved**
