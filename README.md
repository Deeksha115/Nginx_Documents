

## 1_What is Web Servers?

A web server is a software application that serves web pages to web users (browser).

**Example:**
A web server is like a friendly waiter at a restaurant for your computer. Imagine you're at a restaurant, and you want to order some food. You tell the waiter what you want, and the waiter brings it to you. Similarly, a web server is a computer program that waits for requests (orders) from your internet browser when you want to see a website.

![Alt text](images/images.jpeg)

## 2_Types of Web Servers
There are various types of web servers, each serving different purposes. Here are some commonly used web servers:

1. **Nginx**
2. **Apache**
3. **Httpd**
4. **Apache Tomcat**


## 3_Introduction to Nginx

Nginx is a free and open-source web server that helps manage websites. Its main job is to handle incoming web traffic and efficiently deliver website content to users.

## 4_Why Use Nginx?

## Speed and Performance

Nginx makes websites load really fast and work well, even when lots of people are using them. It's great at handling a large number of visitors, so your website stays speedy and responsive.

## Scalability

Nginx is like a superhero for your website that can handle lots of visitors at once without slowing down. It makes sure your website can grow and handle many users at the same time without any problems.

## Reverse Proxy

 Nginx as a bodyguard for your website. When someone wants to visit your site, Nginx stands in front and checks if everything is safe. It can also help share the load among different parts of your website, making sure everything stays secure and works smoothly.

## Load Balancing

Nginx offers load balancing capabilities, distributing traffic among multiple servers to evenly distribute the server load.

## Web Server Security

Nginx helps protect your website from online dangers. These risks can include things like hackers, unauthorized access, data theft, and other online attacks. Through Nginx, you can make your website safe and secure.

## Resource Efficiency

Nginx is like a clever chef who can make a lot of tasty food in a small kitchen without using too many ingredients or energy. In the same way, Nginx efficiently uses your computer's "ingredients" (memory and CPU) so that your website can handle many visitors without needing a lot of computer power. It's like cooking up a big feast without making a mess in the kitchen!


## 5_Key Features

- Fast and efficient.
- Low resource usage.
- Flexible configuration.

**Web Server:**
Nginx is employed as a web server to host and serve web content.

![Alt text](image.png)

**Reverse Proxy Server**:
A reverse proxy is a server that sits between client devices and a web server. It receives requests from clients and forwards those requests to the web server, acting on behalf of the server. The response from the web server is then sent back to the clients.

![Alt text](image-1.png)

**Open-Source**:
 Nginx is open-source, enabling users to modify and distribute the software according to their requirements.


![Alt text](image-2.png)

# 6_Advantages and Disadvantages of Nginx

**Advantage:**
Nginx is fast and can handle a large number of users, thereby enhancing website speed.

**Disadvantage:**
However, Nginx's configuration might be somewhat complex, which could pose a challenge for beginners to understand.

# 7_Why do have use Nginx ?

**Speed and Performance**: 
Nginx efficiently serves websites, providing users with fast responses. Its performance is notably strong, especially for high-traffic websites.

**Scalability:**
 Nginx can easily handle large volumes of traffic, ensuring your website remains scalable, capable of supporting a significant number of users simultaneously.

**Reverse Proxy:**
 It can be utilized as a reverse proxy, offering protection for your web servers and enabling load balancing.

**Load Balancing:**
 Nginx offers load balancing capabilities, distributing traffic among multiple servers to evenly distribute the server load.
 
**Web Server Security:**
 Nginx provides security features, safeguarding your website against various online threats.




## 6_Installation of Nginx

- Provide step-by-step instructions on installing Nginx.

---
sudo apt update
---

```bash
deeksha@devops:~$ sudo apt update
[sudo] password for deeksha:
Hit:1 http://security.ubuntu.com/ubuntu focal-security InRelease
Hit:2 http://in.archive.ubuntu.com/ubuntu focal InRelease
Get:3 http://in.archive.ubuntu.com/ubuntu focal-updates InRelease [114 kB]
Hit:4 http://in.archive.ubuntu.com/ubuntu focal-backports InRelease
Fetched 114 kB in 3s (38.1 kB/s)
Reading package lists... Done
Building dependency tree       
Reading state information... Done
All packages are up to date.
```



---
sudo apt install nginx -y
---

```bash
deeksha@devops:~$ sudo apt install nginx -y
Reading package lists... Done
Building dependency tree       
Reading state information... Done
The following additional packages will be installed:
  libnginx-mod-http-image-filter libnginx-mod-http-xslt-filter libnginx-mod-mail libnginx-mod-stream nginx-common nginx-core
Suggested packages:
  fcgiwrap nginx-doc
The following NEW packages will be installed:
  libnginx-mod-http-image-filter libnginx-mod-http-xslt-filter libnginx-mod-mail libnginx-mod-stream nginx nginx-common nginx-core
0 upgraded, 7 newly installed, 0 to remove and 0 not upgraded.
Need to get 605 kB of archives.
After this operation, 2,141 kB of additional disk space will be used.
Get:1 http://in.archive.ubuntu.com/ubuntu focal-updates/main amd64 nginx-common all 1.18.0-0ubuntu1.4 [37.7 kB]
Get:2 http://in.archive.ubuntu.com/ubuntu focal-updates/main amd64 libnginx-mod-http-image-filter amd64 1.18.0-0ubuntu1.4 [14.8 kB]
Get:3 http://in.archive.ubuntu.com/ubuntu focal-updates/main amd64 libnginx-mod-http-xslt-filter amd64 1.18.0-0ubuntu1.4 [13.0 kB]
Get:4 http://in.archive.ubuntu.com/ubuntu focal-updates/main amd64 libnginx-mod-mail amd64 1.18.0-0ubuntu1.4 [42.9 kB]
Get:5 http://in.archive.ubuntu.com/ubuntu focal-updates/main amd64 libnginx-mod-stream amd64 1.18.0-0ubuntu1.4 [67.4 kB]
Get:6 http://in.archive.ubuntu.com/ubuntu focal-updates/main amd64 nginx-core amd64 1.18.0-0ubuntu1.4 [425 kB]
Get:7 http://in.archive.ubuntu.com/ubuntu focal-updates/main amd64 nginx all 1.18.0-0ubuntu1.4 [3,620 B]
Fetched 605 kB in 4s (169 kB/s)
Preconfiguring packages ...
Selecting previously unselected package nginx-common.
(Reading database ... 182101 files and directories currently installed.)
Preparing to unpack .../
```

---
sudo systemctl status nginx
---

```bash
deeksha@devops:~$ sudo systemctl status nginx
● nginx.service - A high-performance web server and a reverse proxy server
   Loaded: loaded (/lib/systemd/system/nginx.service; enabled; vendor preset: enabled)
   Active: active (running) since Mon 2023-11-20 16:28:26 IST; 10s ago
     Docs: man:nginx(8)
 Main PID: 41697 (nginx)
    Tasks: 2 (limit: 2313)
   Memory: 5.4M
   CGroup: /system.slice/nginx.service
           ├─41697 nginx: master process /usr/sbin/nginx -g daemon on; master_process on;
           └─41698 nginx: worker process
Nov 20 16:28:26 jatin1 systemd[1]: Starting A high-performance web server and a reverse proxy server...
Nov 20 16:28:26 jatin1 systemd[1]: Started A high-performance web server and a reverse proxy server.

```


---
sudo systemctl enable nginx
---

```bash
deeksha@devops:~$ sudo systemctl enable nginx
[sudo] password for deeksha:
Synchronizing state of nginx.service with SysV service script with /lib/systemd/systemd-sysv-install.
Executing: /lib/systemd/systemd-sysv-install enable nginx

```

---
Access Locally: Open a web browser and navigate to [localhost](http://localhost).
---

![Alt text](image-4.png)

# 9. Defaults Files, Folders, and Ports

- **Configuration:**
  `/etc/nginx/nginx.conf`

- **Default Web Root:**
  `/var/www/html/`

- **Default Port:**
  `80`

- **Default Port with SSL:**
  `443`
