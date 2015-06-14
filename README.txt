sudo aptitude install fail2ban ipset

# modify jail.local, set ignoreip and email address

sudo cp jail.local /etc/fail2ban

sudo cp iptables-blocktype.local iptables-ipset*conf /etc/fail2ban/action.d

sudo cp sshban.conf /etc/fail2ban/filter.d

sudo fail2ban start
