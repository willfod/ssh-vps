# ssh-vps
vps+Finalshell教程
FinalShell下载：https://wa6.lanzoui.com/ihjg2y3h14j
FinalShell-MAC版下载：https://wa6.lanzoui.com/iPeC7y3hryf
摘录油管大佬的教程
脚本来自大佬：
VPS服务器系统选择 Debian10或以上
******************************
阿里云不需要，如果是甲骨文云，需要ubuntu转root
需要下面额外两行代码
sudo -i
wget -N https://cdn.jsdelivr.net/gh/Misaka-blog/rootLogin@master/root.sh && chmod -R 777 root.sh && bash root.sh
---------------------------------------------------------
如果你是阿里云等root系统，则：
#更新系统
apt update -y
apt install -y curl
apt install -y socat

#安装脚本
curl https://get.acme.sh | sh
~/.acme.sh/acme.sh --register-account -m willfod3000@outlook.com

#放行80端口
iptables -I INPUT -p tcp --dport 80 -j ACCEPT

#申请证书
~/.acme.sh/acme.sh  --issue -d jgw2.willfod.tk   --standalone
~/.acme.sh/acme.sh --installcert -d jgw2.willfod.tk --key-file /root/private.key --fullchain-file /root/cert.crt

#Xray一键代码
bash <(curl -Ls https://raw.githubusercontent.com/vaxilu/x-ui/master/install.sh)
#放行端口
iptables -I INPUT -p tcp --dport 54321 -j ACCEPT
iptables -I INPUT -p tcp --dport 443 -j ACCEPT
*****
私钥路径：/root/private.key
公钥路径：/root/cert.crt
-------------------------------------------------------------




