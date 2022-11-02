# plan9

plan9 related foo

:::toc

## instant cpu server from livecd

<a href="https://plan9.io/wiki/plan9/Drawterm_to_your_terminal/index.html">https://plan9.io/wiki/plan9/Drawterm_to_your_terminal/index.html</a>

> INSTANT CPU SERVER FROM LIVE CD
> This assumes DHCP internet service. Change the ip/ipconfig line if needed.

> term% ip/ipconfig
> term% auth/factotum
> term% echo 'key proto=p9sk1 dom=livecd user=glenda !password=password' >/mnt/factotum/ctl
> term% aux/listen1 -t tcp!*!17010 /bin/cpu -R &

> This shortcut works on any Plan 9 system that isn't already running a standard authserver + keyfs. It works because starting listen1 with the -t flag keeps the factotum available in the namespace of the cpu listener for direct authentication. Drawterm from another OS will connect as usual. CPU from Plan 9 requires an auth server to validate the key.

> (There seems to be a "direct auth" trick drawterm does that CPU(1) does not. It would be nice if CPU(1) also could connect without an authserver with this setup.)

## Network

### enable networking

using DHCP

> ip/ipconfig

manually

> ip/ipconfig -g <your-gateway> ether /net/ether0 <your-ip-address> <your-subnet-mask>

### get networking information

> cat /net/ndb

lists, the ip, mask, sysname, dns servers, ...
