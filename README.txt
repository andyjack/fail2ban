sudo aptitude install fail2ban ipset
sudo service fail2ban stop

# modify jail.local, set ignoreip and email address

sudo cp jail.local /etc/fail2ban

sudo cp iptables-blocktype.local iptables-ipset*conf /etc/fail2ban/action.d

sudo cp sshban.conf /etc/fail2ban/filter.d

sudo service fail2ban start

# to view blocked ips
sudo less /etc/fail2ban/ip.blocklist.ssh-repeater
sudo ipset list
