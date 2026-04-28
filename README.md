# ce-lab-launch-first-ec2-SUBMIT


Step 1: Find Your IP Address
Write down your IP: 145.90.65.82     (you'll need this!)

Step 2: Create an SSH Key Pair
Expected outcome: You have a private key file saved securely on your computer.

Command:
[ec2-user@ip-172-31-32-50 ~]$ cat ~/.ssh/authorized_keys

Step 6: Explore Your Instance
Command
[ec2-user@ip-172-31-32-50 ~]$ cat /etc/os-release


Output:
NAME="Amazon Linux"
VERSION="2023"
ID="amzn"
ID_LIKE="fedora"
VERSION_ID="2023"
PLATFORM_ID="platform:al2023"
PRETTY_NAME="Amazon Linux 2023.11.20260413"
ANSI_COLOR="0;33"
CPE_NAME="cpe:2.3:o:amazon:amazon_linux:2023"
HOME_URL="https://aws.amazon.com/linux/amazon-linux-2023/"
DOCUMENTATION_URL="https://docs.aws.amazon.com/linux/"
SUPPORT_URL="https://aws.amazon.com/premiumsupport/"
BUG_REPORT_URL="https://github.com/amazonlinux/amazon-linux-2023"
VENDOR_NAME="AWS"
VENDOR_URL="https://aws.amazon.com/"
SUPPORT_END="2029-06-30"


Command
[ec2-user@ip-172-31-32-50 ~]$ free -h

Output: 
               total        used        free      shared  buff/cache   available
Mem:           916Mi       161Mi       383Mi       0.0Ki       371Mi       612Mi
Swap:             0B          0B          0B
[ec2-user@ip-172-31-32-50 ~]$ df -h
Filesystem        Size  Used Avail Use% Mounted on
devtmpfs          4.0M     0  4.0M   0% /dev
tmpfs             459M     0  459M   0% /dev/shm
tmpfs             184M  448K  183M   1% /run
/dev/nvme0n1p1    8.0G  1.7G  6.3G  21% /
tmpfs             459M     0  459M   0% /tmp
/dev/nvme0n1p128   10M  1.3M  8.7M  13% /boot/efi
tmpfs              92M     0   92M   0% /run/user/1000

Command: 
sudo systemctl status httpd

Output: 
● httpd.service - The Apache HTTP Server
     Loaded: loaded (/usr/lib/systemd/system/httpd.service; enabled; preset: disabled)
     Active: active (running) since Mon 2026-04-27 10:53:24 UTC; 19min ago
       Docs: man:httpd.service(8)
   Main PID: 19679 (httpd)
     Status: "Total requests: 0; Idle/Busy workers 100/0;Requests/sec: 0; Bytes served/sec:   0 B/sec"
      Tasks: 177 (limit: 1014)
     Memory: 13.5M
        CPU: 1.056s
     CGroup: /system.slice/httpd.service
             ├─19679 /usr/sbin/httpd -DFOREGROUND
             ├─19816 /usr/sbin/httpd -DFOREGROUND
             ├─19817 /usr/sbin/httpd -DFOREGROUND
             ├─19818 /usr/sbin/httpd -DFOREGROUND
             └─19819 /usr/sbin/httpd -DFOREGROUND

Apr 27 10:53:24 ip-172-31-32-50.eu-north-1.compute.internal systemd[1]: Starting httpd.service - The Apache HTTP Server...
Apr 27 10:53:24 ip-172-31-32-50.eu-north-1.compute.internal systemd[1]: Started httpd.service - The Apache HTTP Server.
Apr 27 10:53:24 ip-172-31-32-50.eu-north-1.compute.internal httpd[19679]: Server configured, listening on: port 80

Command: 
ip addr show


Output: 
1: lo: <LOOPBACK,UP,LOWER_UP> mtu 65536 qdisc noqueue state UNKNOWN group default qlen 1000
    link/loopback 00:00:00:00:00:00 brd 00:00:00:00:00:00
    inet 127.0.0.1/8 scope host lo
       valid_lft forever preferred_lft forever
    inet6 ::1/128 scope host noprefixroute 
       valid_lft forever preferred_lft forever
2: ens5: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 9001 qdisc mq state UP group default qlen 1000
    link/ether 0a:05:ca:1e:a1:e9 brd ff:ff:ff:ff:ff:ff
    altname enp0s5
    altname eni-03c5e8c7cada93288
    altname device-number-0.0
--did not paste credentials--






