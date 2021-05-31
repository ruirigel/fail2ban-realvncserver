# fail2ban-realvncserver

To enable fail2ban for realvncserver add realvncserver-auth.conf to /etc/fail2ban/filter.d
and add tthe following to /etc/fail2ban/jail.conf
```
[realvncserver-auth]
enabled = true
port = 5900
filter = realvncserver-auth
logpath = /var/log/vncserver-x11.log        
bantime = 86400
findtime = 3600
maxretry = 3
```

