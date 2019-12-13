## Usefule Server Commands

check for enabled services
```
systemctl list-unit-files | grep enabled
```

check for running services
```
systemctl | grep running
```

check multiple servers at once via ssh
```
alias sc='for a in `seq -w 01 07`; do echo <server-name->$a; ssh <user>@<server-name->$a.<domain.com> "hostname;systemctl status <service>"; done'
```