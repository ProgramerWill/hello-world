# hello world project

   my first github project.

### 20210320 Sat, Solna

https://kifarunix.com/how-to-setup-squid-proxy-basic-authentication-with-username-and-password/

how to config squid authentication.

Configure Squid Proxy Authentication
Since all seems fine, proceed to setup squid proxy basic authentication. Open the squid configuration file for editing and add the following lines.

auth_param basic program /usr/lib64/squid/basic_ncsa_auth /etc/squid/.squid_users
auth_param basic children 5
auth_param basic realm Proxy Authentication Required
auth_param basic credentialsttl 2 hours
auth_param basic casesensitive off
acl auth_users proxy_auth amos john
http_access allow auth_users


### 20201210 Thu, Kista
   Try to make a ssh tunnel between linux in office and linux at home.
    office linux : 
    ssh -R 8080:localhost:22 ssh://wyy.changeip.org:10022
    then at home linux, we can see,
    home linux will listen 8080(http-alt) port and will forward any connect to this port to 
    the office linux 22 port, it's a connect to ssh again. 
    Then we can see
      office linux ssh A --> home linux --> home linux new ssh to local 8080 port --> through ssh A to office linux
      22 port ---> home linux connect to office linux ssh server and build ssh B.
      
    It's quite interest, isn't it?

    └─$ ss -ta
State          Recv-Q      Send-Q           Local Address:Port                Peer Address:Port          Process      
LISTEN         0           128                  127.0.0.1:http-alt                 0.0.0.0:*                          
LISTEN         0           128                    0.0.0.0:ssh                      0.0.0.0:*                          
ESTAB          0           0                192.168.0.100:ssh                62.119.167.46:2058                       
ESTAB          0           96               192.168.0.100:ssh                62.119.167.46:2060                       
LISTEN         0           128                      [::1]:http-alt                    [::]:*                          
LISTEN         0           128                       [::]:ssh                         [::]:*                          
TIME-WAIT      0           0                        [::1]:52172                      [::1]:http-alt



### 20201209 Wed, Solna
   I just start to use git again. 
   I have set up a kali linux PC just to learn how to make penertration test.
Network security is very important.
   Even for my Kali server just built there are a lot of attempt to connect my sshd server.
   I can use sudo lastb -n 30 to check the attempting IPs.

---
### 20191118 Mon, Kista
   how to query the archlinux startup command line
$ cat /proc/cmdline
BOOT_IMAGE=/vmlinuz-linux root=UUID=c4b1bb3d-2a51-4764-a7e9-c161a83889c2 rw loglevel=3 quiet


### 20190129 Mon, Xi'an
   Today, I fixed the issues of my archlinux after last pacman -Syu update.
   two libraries are missed(libreadline.so.7 and libidn2.so.0) by the beneath steps,
   1. boot with kernel parameters systemd.unit=multi-user.target
   2. goes to /var/cache/pacman/pkg/ and exatrac the missed two libraries from readline.* and libidn2.*
   3. cp the lib to /usr/lib, and make two soft symbolic links.
   4. telinit 5, goes to Xwindow mode.
   



### 20181226 Tues, Xi'an

today is the birthday of Chiarman Mao, it's a big day. And in this day, I am exploring my git project on archlinux platform.
the issue I have met.
1. Unexpected reschedules of offline CPU0 --- disable BIOS funtions keys, disable hyper-CPU functions.
2. can not login as root at first time after install ---- I think maybe I forgot the root password. 1) so I use the archlinux iso bootable USB disk to boot, 2) and mount the disk to /mnt,  3) and then use command archchroot /mnt, then use passwd to change the root password. 4) add a new user will. 5) then I login as will and su to root. it works.
3. network configration : pacman to install NetworkManager package.
4. to support chinese. --- 1) 安装字体。2）配置环境变量；3）安装fcitx输入法，sunpinyin；4）运行 fcitx-diagnose诊断；还是不行，最后重启后输入法可以激活工作。
5. to test github branch pull request.

---
### 20180207 ### 


goutongpai / 2018G0208t
qq 3491416405
goutongpai@qq.com
	

一个月内可申请修改1次

本月还可修改1次


使用 “邮我” 功能

<a target="_blank" href="http://mail.qq.com/cgi-bin/qm_share?t=qm_mailme&email=ya6mvL2mp665qKCJuLjnqqak" style="text-decoration:none;"><img src="http://rescdn.qqmail.com/zh_CN/htmledition/images/function/qm_open/ico_mailme_02.png"/></a>
