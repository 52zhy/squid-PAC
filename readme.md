[PAC](https://www.rpsofts.com/vvv)
=======
����Ŀ��Ҫ����������ù���VPS���Э��������

��лhttps://pac.itzmx.com/  ����itzmx�޸ġ�

����������
==============
�� 25 �˿ڴ http/https ����


Ubuntu����Ҫһ��һ�и��ư�װ��:
-------
> apt-get -y install squid
curl http://www.rpsofts.com/vvv/squid/ubuntu-squid.conf
/etc/squid3/squid.conf
mkdir -p /var/cache/squid
chmod -R 777 /var/cache/squid
service squid3 stop
squid3 -z
service squid3 restart



CentOS 6.7 x64���Ƽ��ô�ϵͳ��:
-------
> setenforce 0
ulimit -n 1048576
echo "* soft nofile 1048576" >> /etc/security/limits.conf
echo "* hard nofile 1048576" >> /etc/security/limits.conf
echo "alias net-pf-10 off" >> /etc/modprobe.d/dist.conf
echo "alias ipv6 off" >> /etc/modprobe.d/dist.conf
killall sendmail
/etc/init.d/postfix stop
chkconfig --level 2345 postfix off
yum -y install squid
wget -O /etc/squid/squid.conf http://wwww.rpsofts.com/vvv/squid/centos-squid.conf
mkdir -p /var/cache/squid
chmod -R 777 /var/cache/squid
squid -z
service squid restart
chkconfig --level 2345 squid on


װ���ǵ�reboot�����·�����ȷ����Ч��

Ȼ��ʹ�� PAC�Ҽ����Ϊ PAC �ļ����޸����е�IP��ַΪ��ķ�����IP���ɡ�

ע�������DNS�޸ĳ�8.8.8.8�������ļ�Ŀǰǿ��ָ����DNS�����������޸ģ�

�������٣���ҳ���ٶȷ�ʮ����Ч������