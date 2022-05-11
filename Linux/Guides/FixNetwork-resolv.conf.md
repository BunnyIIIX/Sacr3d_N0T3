## Resolving timed out after 10000 milliseconds

After a lot of hours trying wget, aria2 and curl, with a lot
of options, I just stopped observing pacman output behaviour
in the console.
Seemed that it was a DNS lookup problem but, in my
resolv.conf, the specified nameserver was my home router.
Anyway, I changed that specifying google's nameservers; is
working now. It's a weird thing because in my homerouter I
was already using google's nameservers.
Now I can open the repos in browser without lag.

Example of my resolv.conf:

Before:
```conf
# home router nameserver
nameserver 192.168.0.1
```

After:
```conf
#Google nameservers
nameserver 8.8.8.8
nameserver 8.8.4.4
```
