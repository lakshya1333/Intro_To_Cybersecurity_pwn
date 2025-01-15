## Level 1:
Send an HTTP request using curl:

```bash
curl localhost 80
```

## Level 2:
Send an HTTP request using nc:
```bash
hacker@talking-web~level2:~$ nc localhost 80
GET /

pwn.college{AUOWQqUx4RZThrLuZkG_Oa1X31X.dljNyMDLxkTM0kzW}
```

## Level 3:
Send an HTTP request using python:

```bash
Python script:
import requests as r

host = "http://127.0.0.1"

response = r.get(host)
print(response.text)
```

## Level 4:
Set the host header in an HTTP request using curl:

```bash
curl -H "Host: 44b23e94068ce7121fcf775c7f9fe564" localhost 80
```

## Level 5:
Set the host header in an HTTP request using nc:

```bash
Created a file request:
hacker@talking-web~level5:~/web$ cat request
GET / HTTP/1.1
Host: abda55d1ff5d4d903adafa213a230388

hacker@talking-web~level5:~/web$ cat request | nc localhost 80
HTTP/1.1 200 OK
Server: Werkzeug/3.0.6 Python/3.8.10
Date: Wed, 15 Jan 2025 18:52:26 GMT
Content-Length: 58
Server: pwn.college
Connection: close
pwn.college{0xU7F4bdeU3DValDe6NVBv5wUpn.dJzNyMDLxkTM0kzW}
```


