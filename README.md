# chfagent-systemd

To grab these files for use on RHEL compatable systemd servers, run the following as root:

```
git clone https://github.com/learhy/chfagent-systemd.git
cd chfagent-systemd
cp chfagent.service /etc/systemd/system
cp chfagent.sh /usr/bin
```
You will then need to modify line 13 of `/usr/bin/chfagent/sh` to set your API key, API email address and any other flags required:

```
cmd="chfagent -api_email=serviceacct_email@example.com -api_token=insertokenhere -type=proxy -host=0.0.0.0"
```

