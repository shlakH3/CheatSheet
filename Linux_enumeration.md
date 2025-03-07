# カーネル
~~~
uname -a
~~~

# ディストリビューション
~~~
/etc/issue
~~~

~~~
/etc/*release
~~~

# CPU
~~~
/proc/cpuinfo
~~~

~~~
lscpu
~~~

# ストレージ
~~~
df -h
~~~

# ユーザー
~~~
whoami
~~~

~~~
who
~~~
![image](https://github.com/user-attachments/assets/b7cb6db9-b366-4842-9412-29ec49e8939a)

~~~
w
~~~
![image](https://github.com/user-attachments/assets/f9e7cc81-8bde-471d-be25-6432ed0b6a46)

~~~
/etc/passwd
~~~

~~~
lastlog
~~~
![image](https://github.com/user-attachments/assets/c74b22bc-cf96-4153-aa4b-69802157b360)

# グループ
~~~
groups
~~~

#SUDO
~~~
sudo -l
~~~

# ネットワーク全般
Debian
~~~
/etc/network/interface
~~~

Redhat
~~~
/etc/sysconfig/network-scripts
~~~

Ubuntu
~~~
/etc/netplan
~~~

~~~
network:
  ethernets:
    ens160:
      addresses:
      - 172.17.50.177/20
      nameservers:
        addresses:
          - 172.17.50.22
          - 172.17.50.23
        search: []
      routes:
      - to: default
        via: 172.17.48.1
  version: 2
~~~

# IPアドレス
~~~
ip a
~~~

~~~
ifconfig
~~~

# ホスト名
一時的な設定かもしれない
~~~
hostname
~~~

永久
~~~
/etc/hostname
~~~

# DNS
~~~
/etc/hosts
~~~

Ubuntuの場合は[../run/systemd/resolve/stub-resolv.conf]のシンボリックリンク
~~~
/etc/resolv.conf
~~~

Ubuntu DHCP
~~~
/run/systemd/resolve/resolv.conf
~~~

~~~
dig any <domain>
~~~
~~~
host <domain>
~~~

# 経路
~~~
traceroute <dest>
~~~

プリインストールされている
~~~
tracepath -b <dest>
~~~

# ポート
~~~
netstat -tlna
~~~

# ルーティング
~~~
route
~~~

~~~
netstat -r
~~~

# プロセス
~~~
ps -aux
~~~

~~~
pgrep <Process name>
~~~

# SUID
~~~
find / -perm 4000 -type f 2>/dev/null
~~~

# cron
~~~
crontab -l
~~~

~~~
/etc/crontab
~~~



