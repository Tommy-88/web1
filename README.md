# web1
awk -F: '{print "user",$1,"has id",$3}' /etc/passwd >> ~/work5.log

sudo chage -l root | head -n 1 » ~/work5.log

awk -F: '{ORS=","} {print $1} END {print "\n"}' /etc/group >> ~/work5.log

echo 'Be careful!' >> /etc/skel/readme.txt

useradd u1 -p $(openssl passwd -crypt 12345678)

groupadd g1

usermod -a -G g1 u1

id u1 >> ~/work5.log

usermod -a -G g1 vitalyboytsov

grep g1 /etc/group | awk -F : '{print $4}' >> ~/work5.log

#usermod -s /usr/bin/mc u1

useradd u2 -p $(openssl passwd -crypt 87654321)

mkdir /home/test13
cp ~/work5.log /home/test13/work5-1.log
cp ~/work5.log /home/test13/work5-2.log

groupadd g2
usermod -a -G g2 u1
usermod -a -G g2 u2
chown u1:g2 /home/test13 -R
chmod 750 /home/test13 -R

mkdir /home/test15
chown u1 /home/test15
chmod 1777 /home/test15

cp /bin/nano /home/test15/nano
chmod 4111 /home/test15/nano
