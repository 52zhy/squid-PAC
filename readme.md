https://www.rpsofts.com/vvv
[PAC](https://www.rpsofts.com/vvv)
=======
����Ŀ��Ҫ����������ù���VPS���Э��������

��лhttp://bbs.itzmx.com/thread-8815-1-1.html  ���Ļ���itzmx�޸ġ�

# PAC��ַ
����https://rplog.qiniudn.com/o_1a1bdhi212lroks75o19m3aha.pac
����https://rplog.qiniudn.com/o_1a1bbteeq4q34427ev2ndfra.pac
# ʹ�÷���
�Ƚ���һ�����ø���ϵͳ����ķ�����
## Windows
Internetѡ�� -> ���� ѡ� -> ����������(����ǵ��Բ�������, �����'����') -> ʹ���Զ����ýű� -> ����PAC��ַ -> ȷ��
![](http://rplog.qiniudn.com/o_1a1begcb49dn1f151fih19se1jsla.jpg)
## Mac OS X
ϵͳ���� -> ���� -> �߼� -> ���� -> �Զ��������� -> URL������PAC��ַ -> ��

## IOS (IPhone/IPad)
������, ѡ��Wi-Fi
ѡ��ǰʹ�õ��ȵ�
![](http://i3.tietuku.com/2204fd1ef2747bd4.png)
�ϵ�������Ĵ������ã�ѡ��"�Զ�"����дPAC��ַ 
![](http://i3.tietuku.com/a5a70098da4ea3f0.png)
## Android
��׿5.0���ϰ汾 ʹ�÷���ͬƻ�������ڰ汾��Ҫʹ�õ��������

���д���������
==============
�� 25 �˿ڴ http/https ����


Ubuntu����Ҫһ��һ�и��ư�װ��:
-------
	apt-get -y install squid
	curl http://www.rpsofts.com/vvv/squid/ubuntu-squid.conf  > /etc/squid3/squid.conf
	mkdir -p /var/cache/squid
	chmod -R 777 /var/cache/squid
	service squid3 stop
	squid3 -z
	service squid3 restart


CentOS 6.7 x64���Ƽ��ô�ϵͳ��:
-------
	setenforce 0
	ulimit -n 1048576
	echo "* soft nofile 1048576" >> /etc/security/limits.conf
	echo "* hard nofile 1048576" >> /etc/security/limits.conf
	echo "alias net-pf-10 off" >> /etc/modprobe.d/dist.conf
	echo "alias ipv6 off" >> /etc/modprobe.d/dist.conf
	killall sendmail
	/etc/init.d/postfix stop
	chkconfig --level 2345 postfix off
	yum -y install squid
	wget -O /etc/squid/squid.conf http://www.rpsofts.com/vvv/squid/centos-squid.conf
	mkdir -p /var/cache/squid
	chmod -R 777 /var/cache/squid
	squid -z
	service squid restart
	chkconfig --level 2345 squid on


װ���ǵ�reboot�����·�����ȷ����Ч��

Ȼ��ʹ��[ PAC](https://rplog.qiniudn.com/o_1a1bdhi212lroks75o19m3aha.pac " PAC")�Ҽ����Ϊ PAC �ļ����޸����е�IP��ַΪ��ķ�����IP���ɡ�

ע�������DNS�޸ĳ�8.8.8.8�������ļ�Ŀǰǿ��ָ����DNS�����������޸ģ�

�������٣���ҳ���ٶȷ�ʮ����Ч������