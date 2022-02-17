# ErpNext Install Script

Make sure to execute these commands on a new user with sudo access

```bash
adduser next
usermod -aG sudo next
sudo su next
```

run the following

```bash
export LC_ALL=C.UTF-8
sudo apt-get install software-properties-common
sudo add-apt-repository ppa:deadsnakes/ppa
sudo apt-get install python3.6
wget https://gist.githubusercontent.com/Muzzy73/6297904cf8171d04902e25b9dc1fc447/raw/8e8d65b53e96f608dc344ccb92f7dd638246e8e9/install.py
sudo python3 install.py --production --user next --version 13 --site mysite.local --mysql-root-password next --admin-password next --verbose
```

Start Frappe Bench

```bash
cd frappe-bench
bench start
```