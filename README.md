# what

what is an improved version of the `w` tool. It finds all processes
associated with a TTY (not just those registered in wtmp), and reports
all users that are running anything. In particular, unlike `w`, `what`
will also shows things running in detached screens/tmuxen. 

Example output:

```console
$ ./what 
 up 23m56s   4 users  load 0.65 0.41 0.23  procs 1/403
USER     TTY      LOGIN  INPUT OUTPUT WHAT
root     tty1    23m53s 23m53s 23m53s /sbin/agetty --noclear tty1 linux 
root     tty7    23m53s 23m53s 23m53s /usr/lib/xorg-server/Xorg -nolisten tcp vt07 -auth /var/run/slim.auth 
jon      pts/0    9m36s     2s     2s python2 ./what 
root     none    177 more processes
jon      none    42 more processes
```
