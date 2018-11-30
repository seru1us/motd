JUST FORKED THIS TO KEEP TRACK OF MY OWN CHANGES IN MY SCRIPTS.

I am using this to document my own MOTD. Obviously, all of the original credit goes to:

https://github.com/yboetz/motd

I am adding support for MDADM in place of checking the SMART self-test, since I couldn't get it to write to the logs appropriately.

In order to get your smartd to report correctly to work with this (something that was missing from the original repo) I have used the following configuration for my disks. Just slap this in your /etc/smartd.conf.

```
/dev/sda -a -H -l error -l selftest -r 194 -I 9 -o on -S on -s (S/../.././02|L/../../6/03)

/dev/sdb -a -H -l error -l selftest -r 194 -I 9 -o on -S on -s (S/../.././02|L/../../6/03)

/dev/sdc -a -H -l error -l selftest -r 194 -I 9 -o on -S on -s (S/../.././02|L/../../6/03)

/dev/sdd -a -H -l error -l selftest -r 194 -I 9 -o on -S on -s (S/../.././02|L/../../6/03)

/dev/sde -a -H -l error -l selftest -r 194 -I 9 -o on -S on -s (S/../.././02|L/../../6/03)

/dev/sdf -a -H -l error -l selftest -r 194 -I 9 -o on -S on -s (S/../.././02|L/../../6/03)

/dev/sdg -a -H -l error -l selftest -r 194 -I 9 -o on -S on -s (S/../.././02|L/../../6/03)

/dev/sdh -a -H -l error -l selftest -r 194 -I 9 -o on -S on -s (S/../.././02|L/../../6/03)
```
