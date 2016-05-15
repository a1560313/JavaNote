# Git 安装使用

## 下载

1. windows：[https://git-scm.com/download/win](https://git-scm.com/download/win)

2. centos: `yum install git`

## 使用

1. 
	ssh-keygen -t rsa -C "a1560313"
2. 
	cat ~/.ssh/id_rsa.pub
3.
	copy ssh-rsa code into github sshkey

4. CLONE
	git clone git@github.com:a1560313/Demo.git
5. 
	cd ~/project/Demo

	git add .

	git commit -m "init add"

	git push origin master

