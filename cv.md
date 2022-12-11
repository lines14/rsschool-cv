# My CV

![My CV photo](My-photo/2faHQKPaPRE.jpg)

### Anton Lipatov

#### Intern frontend developer

**Contacts:**
```
phone: +77478595164
discord: Anton Lipatov (@lines14) lines14#6337
telegram: @lines14
email: tamdobro@yandex.ru
```
**About me:**
> *A professional medic by education, but I realized that the world of IT is more interesting and closer to me. I chose Python because everything can be done on it. I don't like to stand still and I'm constantly learning. Now i started to learn Javascript to become a full-stack developer! Practicing in freelance orders for process automation, parsing and systematization of data using Python scripts. working with SQL (writing and debugging queries) and Excel (at the formula level), CRM administration, remote Linux server administration. As a hobby, I am engaged in the administration of network equipment, software configuration, PC assembly and configuration, skiing, visiting bars, music festivals and concerts.*

**Skills:**
```
Python
Git
Docker
SQL
MS Excel
Linux
AWS
Setting up VPS/VDS servers
CRM
Hyper-V
Process automation
Server Administration
Teamwork
Responsibility
Stress resistance
Communication skills
Literacy
Result orientation
```

**Example of my code (Python encrypted echo-server):**
```
import ssl
import socket
import stun
import os
import dotenv

dotenv.load_dotenv()

INTERNAL_HOST_IP = os.environ.get('INTERNAL_HOST_IP')
SOCKET_PORT = os.environ.get('SOCKET_PORT')
SOCKET_PORT = int(SOCKET_PORT)

out = f'connected to {stun.get_ip_info()[1]} => {INTERNAL_HOST_IP}\nПакет возвращён успешно: '

context = ssl.SSLContext(ssl.PROTOCOL_TLS_SERVER)
context.load_cert_chain('/home/lines14/projects/Server-chain-certificate.pem', '/home/lines14/projects/Server-private-key.key')

with socket.socket(socket.AF_INET, socket.SOCK_STREAM) as sock:
    with context.wrap_socket(sock, server_side=True) as ssock:
        ssock.bind(('', SOCKET_PORT))
        ssock.listen(5)

        while True:
            conn, addr = ssock.accept()

            with conn:
                print(f'Connected by {addr}')   

                while True:
                    inn = conn.recv(1024)
                    if not inn:
                        break
                    ssock_version = f'{conn.version()} '
                    conn.sendall(ssock_version.encode() + out.encode() + inn)
```

**You can check my other code and some freelance stuff on:**

> https://github.com/lines14

**Completed projects:**

> This CV

**Education:**
```
Russian State Medical University - family doctor
Moscow Medical College No. 7 - paramedic
Moscow aviation institute - python development, refresher course (https://github.com/lines14/python_course)
```
**English level:**

> B1