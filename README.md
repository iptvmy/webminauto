apt-get -y update && apt-get -y upgrade

apt-get -y install perl libnet-ssleay-perl openssl libauthen-pam-perl libpam-runtime libio-pty-perl apt-show-versions python

wget http://prdownloads.sourceforge.net/webadmin/webmin_1.880_all.deb

dpkg --install webmin_1.880_all.deb

sed -i 's/ssl=1/ssl=0/g' /etc/webmin/miniserv.conf

rm -f webmin_1.880_all.deb

Restart Webmin

service webmin restart
