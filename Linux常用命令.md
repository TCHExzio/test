# Linux常用命令

防火墙相关

- systemctl stop firewalld.service
- systemctl start firewalld.service
- systemctl enable firewalld
- systemctl disable firewalld
- firewall-cmd --reload
- firewall-cmd --zone=public --list-ports
- firewall-cmd --zone=public --add-port=3338/tcp --permanent

复制

- cp -rf
- rm -rf

启动cm

- sudo systemctl start cloudera-scm-server

设置虚拟内存交换

临时生效

- sysctl -w vm.swappiness=10
- echo never > /sys/kernel/mm/transparent_hugepage/defrag
- echo never > /sys/kernel/mm/transparent_hugepage/enabled

永久生效

- echo "vm.swappiness=10">> /etc/sysctl.conf
- echo "echo never > /sys/kernel/mm/transparent_hugepage/defrag" >> /etc/rc.local
- echo "echo never > /sys/kernel/mm/transparent_hugepage/enabled" >> /etc/rc.local

设置文件夹权限

- chown -R cloudera-scm:cloudera-scm /var/lib/cloudera-host-monitor/