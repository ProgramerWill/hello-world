
# hello world project

   my first github project.

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
