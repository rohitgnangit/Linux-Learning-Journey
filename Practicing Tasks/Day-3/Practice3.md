## Process-Service-Management 

```bash
rohit@Rohit-PC:~$ ps
    PID TTY          TIME CMD
    382 pts/0    00:00:00 bash
    596 pts/0    00:00:00 ps
rohit@Rohit-PC:~$ ps -f
UID          PID    PPID  C STIME TTY          TIME CMD
rohit        382     381  0 15:25 pts/0    00:00:00 -bash
rohit        597     382  0 15:26 pts/0    00:00:00 ps -f
rohit@Rohit-PC:~$ ps aux
USER         PID %CPU %MEM    VSZ   RSS TTY      STAT START   TIME COMMAND
root           1  1.0  0.1  21868 13032 ?        Ss   15:25   0:01 /sbin/ini
root           2  0.0  0.0   3180  2204 hvc0     Sl+  15:25   0:00 /init
root           9  0.0  0.0   3196  2128 hvc0     Sl+  15:25   0:00 plan9 --c
root          64  0.3  0.2  58644 15952 ?        S<s  15:25   0:00 /usr/lib/
root         113  0.2  0.0  25184  6556 ?        Ss   15:25   0:00 /usr/lib/
systemd+     182  0.1  0.1  21344 13236 ?        Ss   15:25   0:00 /usr/lib/
systemd+     183  0.1  0.1  91036  7996 ?        Ssl  15:25   0:00 /usr/lib/
root         189  0.0  0.0   4244  2684 ?        Ss   15:25   0:00 /usr/sbin
message+     193  0.0  0.0   9544  5492 ?        Ss   15:25   0:00 @dbus-dae
root         211  0.1  0.1  17984  8892 ?        Ss   15:25   0:00 /usr/lib/
root         234  0.1  0.1 1756104 12972 ?       Ssl  15:25   0:00 /usr/libe
syslog       243  0.0  0.0 222516  5912 ?        Ssl  15:25   0:00 /usr/sbin
root         265  0.0  0.0   3124  1976 tty1     Ss+  15:25   0:00 /sbin/age
root         271  0.1  0.2 107032 23212 ?        Ssl  15:25   0:00 /usr/bin/
root         380  0.0  0.0   3184  1108 ?        Ss   15:25   0:00 /init
root         381  0.0  0.0   3200  1120 ?        S    15:25   0:00 /init
rohit        382  0.0  0.0   6208  5420 pts/0    Ss   15:25   0:00 -bash
root         383  0.0  0.0   6704  4668 pts/1    Ss   15:25   0:00 /bin/logi
rohit        429  0.2  0.1  20340 11432 ?        Ss   15:25   0:00 /usr/lib/
rohit        430  0.0  0.0  21160  3568 ?        S    15:25   0:00 (sd-pam)
rohit        461  0.0  0.0   6080  5392 pts/1    S+   15:25   0:00 -bash
rohit        598  0.0  0.0   8288  4308 pts/0    R+   15:27   0:00 ps aux
rohit@Rohit-PC:~$ top
top - 15:31:42 up 6 min,  1 user,  load average: 0.08, 0.04, 0.01
Tasks:  22 total,   1 running,  21 sleeping,   0 stopped,   0 zombie
%Cpu(s):  0.0 us,  0.0 sy,  0.0 ni,100.0 id,  0.0 wa,  0.0 hi,  0.0 si,  0.
MiB Mem :   7598.6 total,   5825.2 free,    523.3 used,   1401.3 buff/cache
MiB Swap:   2048.0 total,   2048.0 free,      0.0 used.   7075.3 avail Mem

    PID USER      PR  NI    VIRT    RES    SHR S  %CPU  %MEM     TIME+
    381 root      20   0    3200   1120    980 S   0.3   0.0   0:00.01
      1 root      20   0   21868  13032   9608 S   0.0   0.2   0:01.12
      2 root      20   0    3180   2204   2072 S   0.0   0.0   0:00.02
      9 root      20   0    3196   2128   2008 S   0.0   0.0   0:00.00
     64 root      19  -1   66840  15972  14784 S   0.0   0.2   0:00.39
    113 root      20   0   25184   6556   5136 S   0.0   0.1   0:00.26
    182 systemd+  20   0   21344  13236  11108 S   0.0   0.2   0:00.18
    183 systemd+  20   0   91036   8000   7032 S   0.0   0.1   0:00.15
    189 root      20   0    4244   2684   2432 S   0.0   0.0   0:00.00
    193 message+  20   0    9544   5492   4792 S   0.0   0.1   0:00.10
    211 root      20   0   17984   8892   7848 S   0.0   0.1   0:00.14
    234 root      20   0 1756104  12972  10888 S   0.0   0.2   0:00.17
    243 syslog    20   0  222516   5912   4528 S   0.0   0.1   0:00.11
    265 root      20   0    3124   1976   1836 S   0.0   0.0   0:00.01
    271 root      20   0  107032  23212  13756 S   0.0   0.3   0:00.19
    380 root      20   0    3184   1108    980 S   0.0   0.0   0:00.00
    382 rohit     20   0    6208   5420   3640 S   0.0   0.1   0:00.07
    383 root      20   0    6704   4668   3884 S   0.0   0.1   0:00.02
    429 rohit     20   0   20340  11432   9288 S   0.0   0.1   0:00.22
    430 rohit     20   0   21160   3568   1848 S   0.0   0.0   0:00.00
    461 rohit     20   0    6080   5392   3668 S   0.0   0.1   0:00.04
    599 rohit     20   0    9300   5676   3488 R   0.0   0.1   0:00.15












[1]+  Stopped                 top
rohit@Rohit-PC:~$ sleep 300
^Z
[2]+  Stopped                 sleep 300
rohit@Rohit-PC:~$ bg
[2]+ sleep 300 &
rohit@Rohit-PC:~$ nice -n -19 sleep 300 &
[3] 607
rohit@Rohit-PC:~$ nice: cannot set niceness: Permission denied
^C
rohit@Rohit-PC:~$ jobs
[1]+  Stopped                 top
[2]   Running                 sleep 300 &
[3]-  Running                 nice -n -19 sleep 300 &
rohit@Rohit-PC:~$ ps aux
USER         PID %CPU %MEM    VSZ   RSS TTY      STAT START   TIME COMMAND
root           1  0.2  0.1  21868 13032 ?        Ss   15:25   0:01 /sbin/ini
root           2  0.0  0.0   3180  2204 hvc0     Sl+  15:25   0:00 /init
root           9  0.0  0.0   3196  2128 hvc0     Sl+  15:25   0:00 plan9 --c
root          64  0.0  0.2  66840 15976 ?        S<s  15:25   0:00 /usr/lib/
root         113  0.0  0.0  25184  6556 ?        Ss   15:25   0:00 /usr/lib/
systemd+     182  0.0  0.1  21344 13236 ?        Ss   15:25   0:00 /usr/lib/
systemd+     183  0.0  0.1  91036  8000 ?        Ssl  15:25   0:00 /usr/lib/
root         189  0.0  0.0   4244  2684 ?        Ss   15:25   0:00 /usr/sbin
message+     193  0.0  0.0   9544  5492 ?        Ss   15:25   0:00 @dbus-dae
root         211  0.0  0.1  17984  8892 ?        Ss   15:25   0:00 /usr/lib/
root         234  0.0  0.1 1756104 12972 ?       Ssl  15:25   0:00 /usr/libe
syslog       243  0.0  0.0 222516  5912 ?        Ssl  15:25   0:00 /usr/sbin
root         265  0.0  0.0   3124  1976 tty1     Ss+  15:25   0:00 /sbin/age
root         271  0.0  0.2 107032 23212 ?        Ssl  15:25   0:00 /usr/bin/
root         380  0.0  0.0   3184  1108 ?        Ss   15:25   0:00 /init
root         381  0.0  0.0   3200  1120 ?        S    15:25   0:00 /init
rohit        382  0.0  0.0   6208  5420 pts/0    Ss   15:25   0:00 -bash
root         383  0.0  0.0   6704  4668 pts/1    Ss   15:25   0:00 /bin/logi
rohit        429  0.0  0.1  20340 11432 ?        Ss   15:25   0:00 /usr/lib/
rohit        430  0.0  0.0  21160  3568 ?        S    15:25   0:00 (sd-pam)
rohit        461  0.0  0.0   6080  5392 pts/1    S+   15:25   0:00 -bash
rohit        599  0.0  0.0   9300  5676 pts/0    T    15:27   0:00 top
rohit        606  0.0  0.0   3132  1896 pts/0    S    15:31   0:00 sleep 300
rohit        607  0.0  0.0   3132  1904 pts/0    S    15:32   0:00 sleep 300
rohit        628  0.0  0.0   8288  4304 pts/0    R+   15:33   0:00 ps aux
rohit@Rohit-PC:~$ top
top - 15:33:51 up 8 min,  1 user,  load average: 0.01, 0.02, 0.00
Tasks:  25 total,   1 running,  23 sleeping,   1 stopped,   0 zombie
%Cpu(s):  0.0 us,  0.0 sy,  0.0 ni,100.0 id,  0.0 wa,  0.0 hi,  0.0 si,  0.
MiB Mem :   7598.6 total,   5818.9 free,    529.5 used,   1401.4 buff/cache
MiB Swap:   2048.0 total,   2048.0 free,      0.0 used.   7069.2 avail Mem

    PID USER      PR  NI    VIRT    RES    SHR S  %CPU  %MEM     TIME+
    381 root      20   0    3200   1120    980 S   0.7   0.0   0:00.04
      1 root      20   0   21868  13032   9608 S   0.0   0.2   0:01.15
      2 root      20   0    3180   2204   2072 S   0.0   0.0   0:00.02
      9 root      20   0    3196   2128   2008 S   0.0   0.0   0:00.00
     64 root      19  -1   66840  15980  14792 S   0.0   0.2   0:00.40
    113 root      20   0   25184   6556   5136 S   0.0   0.1   0:00.26
    182 systemd+  20   0   21344  13236  11108 S   0.0   0.2   0:00.18
    183 systemd+  20   0   91036   8000   7032 S   0.0   0.1   0:00.15
    189 root      20   0    4244   2684   2432 S   0.0   0.0   0:00.01
    193 message+  20   0    9544   5492   4792 S   0.0   0.1   0:00.10
    211 root      20   0   17984   8892   7848 S   0.0   0.1   0:00.14
    234 root      20   0 1756104  12980  10888 S   0.0   0.2   0:00.18
    243 syslog    20   0  222516   5912   4528 S   0.0   0.1   0:00.11
    265 root      20   0    3124   1976   1836 S   0.0   0.0   0:00.01
    271 root      20   0  107032  23212  13756 S   0.0   0.3   0:00.19
    380 root      20   0    3184   1108    980 S   0.0   0.0   0:00.00
    382 rohit     20   0    6208   5420   3640 S   0.0   0.1   0:00.09
    383 root      20   0    6704   4668   3884 S   0.0   0.1   0:00.02
    429 rohit     20   0   20340  11432   9288 S   0.0   0.1   0:00.23
    430 rohit     20   0   21160   3568   1848 S   0.0   0.0   0:00.00
    461 rohit     20   0    6080   5392   3668 S   0.0   0.1   0:00.04
    599 rohit     20   0    9300   5676   3488 T   0.0   0.1   0:00.15
    606 rohit     20   0    3132   1896   1784 S   0.0   0.0   0:00.00
    607 rohit     20   0    3132   1904   1788 S   0.0   0.0   0:00.00
    629 rohit     20   0    9300   5756   3568 R   0.0   0.1   0:00.00









[4]+  Stopped                 top
rohit@Rohit-PC:~$ jobs
[1]-  Stopped                 top
[2]   Running                 sleep 300 &
[3]   Running                 nice -n -19 sleep 300 &
[4]+  Stopped                 top
rohit@Rohit-PC:~$ nice -n -19 sleep 30
nice: cannot set niceness: Permission denied
^C
rohit@Rohit-PC:~$ jobs
[1]-  Stopped                 top
[2]   Running                 sleep 300 &
[3]   Running                 nice -n -19 sleep 300 &
[4]+  Stopped                 top
rohit@Rohit-PC:~$ nice -n -18 sleep 30
nice: cannot set niceness: Permission denied
^C
rohit@Rohit-PC:~$ nice -n -5 sleep 30
nice: cannot set niceness: Permission denied
^C
rohit@Rohit-PC:~$ nice -n 18 sleep 30
^Z
[5]+  Stopped                 nice -n 18 sleep 30
rohit@Rohit-PC:~$ bg
[5]+ nice -n 18 sleep 30 &
rohit@Rohit-PC:~$ jobs
[1]-  Stopped                 top
[2]   Running                 sleep 300 &
[3]   Running                 nice -n -19 sleep 300 &
[4]+  Stopped                 top
[5]   Running                 nice -n 18 sleep 30 &
rohit@Rohit-PC:~$ nice -n -18 sleep 300
nice: cannot set niceness: Permission denied
^C
[5]   Done                    nice -n 18 sleep 30
rohit@Rohit-PC:~$ jobs
[1]-  Stopped                 top
[2]   Running                 sleep 300 &
[3]   Running                 nice -n -19 sleep 300 &
[4]+  Stopped                 top
rohit@Rohit-PC:~$ nice -n 18 sleep 300
^C
rohit@Rohit-PC:~$ jobs
[1]-  Stopped                 top
[2]   Running                 sleep 300 &
[3]   Running                 nice -n -19 sleep 300 &
[4]+  Stopped                 top
rohit@Rohit-PC:~$ nice -n 18 sleep 300 &
[5] 640
rohit@Rohit-PC:~$ jobs
[1]-  Stopped                 top
[2]   Running                 sleep 300 &
[3]   Running                 nice -n -19 sleep 300 &
[4]+  Stopped                 top
[5]   Running                 nice -n 18 sleep 300 &
rohit@Rohit-PC:~$ ps aux
USER         PID %CPU %MEM    VSZ   RSS TTY      STAT START   TIME COMMAND
root           1  0.1  0.1  21868 13032 ?        Ss   15:25   0:01 /sbin/ini
root           2  0.0  0.0   3180  2204 hvc0     Sl+  15:25   0:00 /init
root           9  0.0  0.0   3196  2128 hvc0     Sl+  15:25   0:00 plan9 --c
root          64  0.0  0.2  66840 15980 ?        S<s  15:25   0:00 /usr/lib/
root         113  0.0  0.0  25184  6556 ?        Ss   15:25   0:00 /usr/lib/
systemd+     182  0.0  0.1  21344 13236 ?        Ss   15:25   0:00 /usr/lib/
systemd+     183  0.0  0.1  91036  8000 ?        Ssl  15:25   0:00 /usr/lib/
root         189  0.0  0.0   4244  2684 ?        Ss   15:25   0:00 /usr/sbin
message+     193  0.0  0.0   9544  5492 ?        Ss   15:25   0:00 @dbus-dae
root         211  0.0  0.1  17984  8892 ?        Ss   15:25   0:00 /usr/lib/
root         234  0.0  0.1 1756104 12996 ?       Ssl  15:25   0:00 /usr/libe
syslog       243  0.0  0.0 222516  5912 ?        Ssl  15:25   0:00 /usr/sbin
root         265  0.0  0.0   3124  1976 tty1     Ss+  15:25   0:00 /sbin/age
root         271  0.0  0.2 107032 23212 ?        Ssl  15:25   0:00 /usr/bin/
root         380  0.0  0.0   3184  1108 ?        Ss   15:25   0:00 /init
root         381  0.0  0.0   3200  1120 ?        S    15:25   0:00 /init
rohit        382  0.0  0.0   6208  5420 pts/0    Ss   15:25   0:00 -bash
root         383  0.0  0.0   6704  4668 pts/1    Ss   15:25   0:00 /bin/logi
rohit        429  0.0  0.1  20340 11432 ?        Ss   15:25   0:00 /usr/lib/
rohit        430  0.0  0.0  21160  3568 ?        S    15:25   0:00 (sd-pam)
rohit        461  0.0  0.0   6080  5392 pts/1    S+   15:25   0:00 -bash
rohit        599  0.0  0.0   9300  5676 pts/0    T    15:27   0:00 top
rohit        606  0.0  0.0   3132  1896 pts/0    S    15:31   0:00 sleep 300
rohit        607  0.0  0.0   3132  1904 pts/0    S    15:32   0:00 sleep 300
rohit        629  0.0  0.0   9300  5756 pts/0    T    15:33   0:00 top
rohit        640  0.0  0.0   3132  1904 pts/0    SN   15:36   0:00 sleep 300
rohit        641 33.3  0.0   8288  4308 pts/0    R+   15:36   0:00 ps aux
rohit@Rohit-PC:~$ sleep 250
^Z[2]   Done                    sleep 300

[6]+  Stopped                 sleep 250
rohit@Rohit-PC:~$ bg
[6]+ sleep 250 &
rohit@Rohit-PC:~$ ps aux
USER         PID %CPU %MEM    VSZ   RSS TTY      STAT START   TIME COMMAND
root           1  0.1  0.1  21868 13032 ?        Ss   15:25   0:01 /sbin/ini
root           2  0.0  0.0   3180  2204 hvc0     Sl+  15:25   0:00 /init
root           9  0.0  0.0   3196  2128 hvc0     Sl+  15:25   0:00 plan9 --c
root          64  0.0  0.2  66840 15980 ?        S<s  15:25   0:00 /usr/lib/
root         113  0.0  0.0  25184  6556 ?        Ss   15:25   0:00 /usr/lib/
systemd+     182  0.0  0.1  21344 13236 ?        Ss   15:25   0:00 /usr/lib/
systemd+     183  0.0  0.1  91036  8000 ?        Ssl  15:25   0:00 /usr/lib/
root         189  0.0  0.0   4244  2684 ?        Ss   15:25   0:00 /usr/sbin
message+     193  0.0  0.0   9544  5492 ?        Ss   15:25   0:00 @dbus-dae
root         211  0.0  0.1  17984  8892 ?        Ss   15:25   0:00 /usr/lib/
root         234  0.0  0.1 1756104 12996 ?       Ssl  15:25   0:00 /usr/libe
syslog       243  0.0  0.0 222516  5912 ?        Ssl  15:25   0:00 /usr/sbin
root         265  0.0  0.0   3124  1976 tty1     Ss+  15:25   0:00 /sbin/age
root         271  0.0  0.2 107032 23212 ?        Ssl  15:25   0:00 /usr/bin/
root         380  0.0  0.0   3184  1108 ?        Ss   15:25   0:00 /init
root         381  0.0  0.0   3200  1120 ?        S    15:25   0:00 /init
rohit        382  0.0  0.0   6208  5420 pts/0    Ss   15:25   0:00 -bash
root         383  0.0  0.0   6704  4668 pts/1    Ss   15:25   0:00 /bin/logi
rohit        429  0.0  0.1  20340 11432 ?        Ss   15:25   0:00 /usr/lib/
rohit        430  0.0  0.0  21160  3568 ?        S    15:25   0:00 (sd-pam)
rohit        461  0.0  0.0   6080  5392 pts/1    S+   15:25   0:00 -bash
rohit        599  0.0  0.0   9300  5676 pts/0    T    15:27   0:00 top
rohit        607  0.0  0.0   3132  1904 pts/0    S    15:32   0:00 sleep 300
rohit        629  0.0  0.0   9300  5756 pts/0    T    15:33   0:00 top
rohit        640  0.0  0.0   3132  1904 pts/0    SN   15:36   0:00 sleep 300
rohit        642  0.0  0.0   3132  1900 pts/0    S    15:37   0:00 sleep 250
rohit        643  0.0  0.0   8288  4332 pts/0    R+   15:37   0:00 ps aux
rohit@Rohit-PC:~$ top
top - 15:38:59 up 13 min,  1 user,  load average: 0.00, 0.02, 0.00
Tasks:  26 total,   1 running,  23 sleeping,   2 stopped,   0 zombie
%Cpu(s):  0.0 us,  0.0 sy,  0.0 ni,100.0 id,  0.0 wa,  0.0 hi,  0.0 si,  0.
MiB Mem :   7598.6 total,   7073.0 free,    528.1 used,    147.1 buff/cache
MiB Swap:   2048.0 total,   2048.0 free,      0.0 used.   7070.6 avail Mem

    PID USER      PR  NI    VIRT    RES    SHR S  %CPU  %MEM     TIME+
      1 root      20   0   21868  13032   9608 S   0.0   0.2   0:01.16
      2 root      20   0    3180   2204   2072 S   0.0   0.0   0:00.02
      9 root      20   0    3196   2128   2008 S   0.0   0.0   0:00.00
     64 root      19  -1   66840  15984  14796 S   0.0   0.2   0:00.42
    113 root      20   0   25184   6556   5136 S   0.0   0.1   0:00.26
    182 systemd+  20   0   21344  13236  11108 S   0.0   0.2   0:00.18
    183 systemd+  20   0   91036   8000   7032 S   0.0   0.1   0:00.17
    189 root      20   0    4244   2684   2432 S   0.0   0.0   0:00.01
    193 message+  20   0    9544   5492   4792 S   0.0   0.1   0:00.11
    211 root      20   0   17984   8892   7848 S   0.0   0.1   0:00.14
    234 root      20   0 1756104  13000  10888 S   0.0   0.2   0:00.20
    243 syslog    20   0  222516   5912   4528 S   0.0   0.1   0:00.11
    265 root      20   0    3124   1976   1836 S   0.0   0.0   0:00.01
    271 root      20   0  107032  23212  13756 S   0.0   0.3   0:00.19
    380 root      20   0    3184   1108    980 S   0.0   0.0   0:00.00
    381 root      20   0    3200   1120    980 S   0.0   0.0   0:00.09
    382 rohit     20   0    6208   5420   3640 S   0.0   0.1   0:00.14
    383 root      20   0    6704   4668   3884 S   0.0   0.1   0:00.02
    429 rohit     20   0   20340  11432   9288 S   0.0   0.1   0:00.23
    430 rohit     20   0   21160   3568   1848 S   0.0   0.0   0:00.00
    461 rohit     20   0    6080   5392   3668 S   0.0   0.1   0:00.04
    599 rohit     20   0    9300   5676   3488 T   0.0   0.1   0:00.15
    629 rohit     20   0    9300   5756   3568 T   0.0   0.1   0:00.00
    640 rohit     38  18    3132   1904   1792 S   0.0   0.0   0:00.00
    642 rohit     20   0    3132   1900   1788 S   0.0   0.0   0:00.00
    644 rohit     20   0    9300   5700   3512 R   0.0   0.1   0:00.07







[3]   Done                    nice -n -19 sleep 300

[7]+  Stopped                 top
rohit@Rohit-PC:~$ jobs
[1]   Stopped                 top
[4]-  Stopped                 top
[5]   Running                 nice -n 18 sleep 300 &
[6]   Running                 sleep 250 &
[7]+  Stopped                 top
rohit@Rohit-PC:~$ ps -f
UID          PID    PPID  C STIME TTY          TIME CMD
rohit        382     381  0 15:25 pts/0    00:00:00 -bash
rohit        599     382  0 15:27 pts/0    00:00:00 top
rohit        629     382  0 15:33 pts/0    00:00:00 top
rohit        640     382  0 15:36 pts/0    00:00:00 sleep 300
rohit        642     382  0 15:37 pts/0    00:00:00 sleep 250
rohit        644     382  0 15:37 pts/0    00:00:00 top
rohit        645     382  0 15:39 pts/0    00:00:00 ps -f
rohit@Rohit-PC:~$ kill -l
 1) SIGHUP       2) SIGINT       3) SIGQUIT      4) SIGILL       5) SIGTRAP
 6) SIGABRT      7) SIGBUS       8) SIGFPE       9) SIGKILL     10) SIGUSR1
11) SIGSEGV     12) SIGUSR2     13) SIGPIPE     14) SIGALRM     15) SIGTERM
16) SIGSTKFLT   17) SIGCHLD     18) SIGCONT     19) SIGSTOP     20) SIGTSTP
21) SIGTTIN     22) SIGTTOU     23) SIGURG      24) SIGXCPU     25) SIGXFSZ
26) SIGVTALRM   27) SIGPROF     28) SIGWINCH    29) SIGIO       30) SIGPWR
31) SIGSYS      34) SIGRTMIN    35) SIGRTMIN+1  36) SIGRTMIN+2  37) SIGRTMIN+3
38) SIGRTMIN+4  39) SIGRTMIN+5  40) SIGRTMIN+6  41) SIGRTMIN+7  42) SIGRTMIN+8
43) SIGRTMIN+9  44) SIGRTMIN+10 45) SIGRTMIN+11 46) SIGRTMIN+12 47) SIGRTMIN+13
48) SIGRTMIN+14 49) SIGRTMIN+15 50) SIGRTMAX-14 51) SIGRTMAX-13 52) SIGRTMAX-12
53) SIGRTMAX-11 54) SIGRTMAX-10 55) SIGRTMAX-9  56) SIGRTMAX-8  57) SIGRTMAX-7
58) SIGRTMAX-6  59) SIGRTMAX-5  60) SIGRTMAX-4  61) SIGRTMAX-3  62) SIGRTMAX-2
63) SIGRTMAX-1  64) SIGRTMAX
rohit@Rohit-PC:~$ kill 9 642
-bash: kill: (9) - Operation not permitted
rohit@Rohit-PC:~$ jobs
[1]   Stopped                 top
[4]-  Stopped                 top
[5]   Running                 nice -n 18 sleep 300 &
[6]   Terminated              sleep 250
[7]+  Stopped                 top
rohit@Rohit-PC:~$ systemctl status ssh
Unit ssh.service could not be found.
[5]   Done                    nice -n 18 sleep 300
rohit@Rohit-PC:~$ jobs
[1]   Stopped                 top
[4]-  Stopped                 top
[7]+  Stopped                 top
rohit@Rohit-PC:~$ systemctl status sshd
Unit sshd.service could not be found.
rohit@Rohit-PC:~$ systemctl status nginx
Unit nginx.service could not be found.
rohit@Rohit-PC:~$ systemctl list-units --type=service
  UNIT                                     LOAD   ACTIVE SUB     DESCRIPTIO>
  console-setup.service                    loaded active exited  Set consol>
  cron.service                             loaded active running Regular ba>
  dbus.service                             loaded active running D-Bus Syst>
  getty@tty1.service                       loaded active running Getty on t>
  keyboard-setup.service                   loaded active exited  Set the co>
  kmod-static-nodes.service                loaded active exited  Create Lis>
  podman-restart.service                   loaded active exited  Podman Sta>
  rsyslog.service                          loaded active running System Log>
  setvtrgb.service                         loaded active exited  Set consol>
  snapd.seeded.service                     loaded active exited  Wait until>
  systemd-journal-flush.service            loaded active exited  Flush Jour>
  systemd-journald.service                 loaded active running Journal Se>
  systemd-logind.service                   loaded active running User Login>
  systemd-modules-load.service             loaded active exited  Load Kerne>
  systemd-remount-fs.service               loaded active exited  Remount Ro>
  systemd-resolved.service                 loaded active running Network Na>
  systemd-sysctl.service                   loaded active exited  Apply Kern>
  systemd-timesyncd.service                loaded active running Network Ti>
  systemd-tmpfiles-setup-dev-early.service loaded active exited  Create Sta>
  systemd-tmpfiles-setup-dev.service       loaded active exited  Create Sta>
  systemd-tmpfiles-setup.service           loaded active exited  Create Vol>
  systemd-udev-trigger.service             loaded active exited  Coldplug A>
  systemd-udevd.service                    loaded active running Rule-based>
  systemd-update-utmp.service              loaded active exited  Record Sys>
  systemd-user-sessions.service            loaded active exited  Permit Use>
  unattended-upgrades.service              loaded active running Unattended>
  user-runtime-dir@1000.service            loaded active exited  User Runti>
  user@1000.service                        loaded active running User Manag>
  wsl-pro.service                          loaded active running Bridge to >

Legend: LOAD   → Reflects whether the unit definition was properly loaded.
        ACTIVE → The high-level unit activation state, i.e. generalization >
        SUB    → The low-level unit activation state, values depend on unit>

29 loaded units listed. Pass --all to see loaded but inactive units, too.
To show all installed unit files use 'systemctl list-unit-files'.
lines 1-37/37 (END)
[8]+  Stopped                 systemctl list-units --type=service
rohit@Rohit-PC:~$ systemctl list-units --type=service --status=running
systemctl: unrecognized option '--status=running'
rohit@Rohit-PC:~$ systemctl list-units --type=service --state=running
  UNIT                        LOAD   ACTIVE SUB     DESCRIPTION            >
  cron.service                loaded active running Regular background prog>
  dbus.service                loaded active running D-Bus System Message Bus
  getty@tty1.service          loaded active running Getty on tty1
  rsyslog.service             loaded active running System Logging Service
  systemd-journald.service    loaded active running Journal Service
  systemd-logind.service      loaded active running User Login Management
  systemd-resolved.service    loaded active running Network Name Resolution
  systemd-timesyncd.service   loaded active running Network Time Synchroniz>
  systemd-udevd.service       loaded active running Rule-based Manager for >
  unattended-upgrades.service loaded active running Unattended Upgrades Shu>
  user@1000.service           loaded active running User Manager for UID 10>
  wsl-pro.service             loaded active running Bridge to Ubuntu Pro ag>

Legend: LOAD   → Reflects whether the unit definition was properly loaded.
        ACTIVE → The high-level unit activation state, i.e. generalization >
        SUB    → The low-level unit activation state, values depend on unit>

12 loaded units listed.
lines 1-19/19 (END)
[9]+  Stopped                 systemctl list-units --type=service --state=running
log file: ^C
rohit@Rohit-PC:~$ systemctl status cron
● cron.service - Regular background program processing daemon
     Loaded: loaded (/usr/lib/systemd/system/cron.service; enabled; preset:>
     Active: active (running) since Mon 2026-09-07 15:25:27 UTC; 35min ago
       Docs: man:cron(8)
   Main PID: 189 (cron)
      Tasks: 1 (limit: 9105)
     Memory: 408.0K (peak: 1.5M)
        CPU: 18ms
     CGroup: /system.slice/cron.service
             └─189 /usr/sbin/cron -f -P

Sep 07 15:25:27 Rohit-PC systemd[1]: Started cron.service - Regular backgro>
Sep 07 15:25:27 Rohit-PC (cron)[189]: cron.service: Referenced but unset en>
Sep 07 15:25:27 Rohit-PC cron[189]: (CRON) INFO (pidfile fd = 3)
Sep 07 15:25:27 Rohit-PC cron[189]: (CRON) INFO (Running @reboot jobs)
lines 1-15/15 (END)
[10]+  Stopped                 systemctl status cron
rohit@Rohit-PC:~$ systemctl stop cron
Failed to stop cron.service: Interactive authentication required.
See system logs and 'systemctl status cron.service' for details.
rohit@Rohit-PC:~$ journelctl -u cron
Command 'journelctl' not found, did you mean:
  command 'journalctl' from deb systemd (255.4-1ubuntu8.16)
Try: sudo apt install <deb name>
rohit@Rohit-PC:~$ journalctl -u cron
Aug 03 12:17:01 Rohit-PC CRON[1318]: pam_unix(cron:session): session opened>
Aug 03 12:17:01 Rohit-PC CRON[1319]: (root) CMD (cd / && run-parts --report>
Aug 03 12:17:01 Rohit-PC CRON[1318]: pam_unix(cron:session): session closed>
Aug 03 13:05:41 Rohit-PC systemd[1]: Stopping cron.service - Regular backgr>
Aug 03 13:05:41 Rohit-PC systemd[1]: cron.service: Deactivated successfully.
Aug 03 13:05:41 Rohit-PC systemd[1]: Stopped cron.service - Regular backgro>
-- Boot 26af2d3ed481487c9a250e32dd40640c --
Aug 04 05:40:37 Rohit-PC systemd[1]: Started cron.service - Regular backgro>
Aug 04 05:40:37 Rohit-PC (cron)[187]: cron.service: Referenced but unset en>
Aug 04 05:40:37 Rohit-PC cron[187]: (CRON) INFO (pidfile fd = 3)
Aug 04 05:40:37 Rohit-PC cron[187]: (CRON) INFO (Running @reboot jobs)
Aug 04 06:17:01 Rohit-PC CRON[623]: pam_unix(cron:session): session opened >
Aug 04 06:17:01 Rohit-PC CRON[624]: (root) CMD (cd / && run-parts --report >
Aug 04 06:17:01 Rohit-PC CRON[623]: pam_unix(cron:session): session closed >
Aug 04 06:25:01 Rohit-PC CRON[639]: pam_unix(cron:session): session opened >
Aug 04 06:25:01 Rohit-PC CRON[640]: (root) CMD (test -x /usr/sbin/anacron |>
Aug 04 06:25:01 Rohit-PC CRON[639]: pam_unix(cron:session): session closed >
Aug 04 07:17:01 Rohit-PC CRON[820]: pam_unix(cron:session): session opened >
Aug 04 07:17:01 Rohit-PC CRON[821]: (root) CMD (cd / && run-parts --report >
Aug 04 07:17:01 Rohit-PC CRON[820]: pam_unix(cron:session): session closed >
Aug 04 09:17:01 Rohit-PC CRON[982]: pam_unix(cron:session): session opened >
Aug 04 09:17:01 Rohit-PC CRON[983]: (root) CMD (cd / && run-parts --report >
Aug 04 09:17:01 Rohit-PC CRON[982]: pam_unix(cron:session): session closed >
Aug 04 10:17:01 Rohit-PC CRON[1047]: pam_unix(cron:session): session opened>
Aug 04 10:17:01 Rohit-PC CRON[1048]: (root) CMD (cd / && run-parts --report>
Aug 04 10:17:01 Rohit-PC CRON[1047]: pam_unix(cron:session): session closed>
Aug 04 12:17:01 Rohit-PC CRON[1220]: pam_unix(cron:session): session opened>
Aug 04 12:17:01 Rohit-PC CRON[1221]: (root) CMD (cd / && run-parts --report>
Aug 04 12:17:01 Rohit-PC CRON[1220]: pam_unix(cron:session): session closed>
Aug 04 13:08:40 Rohit-PC systemd[1]: Stopping cron.service - Regular backgr>
Aug 04 13:08:40 Rohit-PC systemd[1]: cron.service: Deactivated successfully.
Aug 04 13:08:40 Rohit-PC systemd[1]: Stopped cron.service - Regular backgro>
-- Boot e5622b25adcd4c6eb2b5434120cefa48 --
Aug 05 09:17:34 Rohit-PC systemd[1]: Started cron.service - Regular backgro>
Aug 05 09:17:34 Rohit-PC (cron)[187]: cron.service: Referenced but unset en>
Aug 05 09:17:34 Rohit-PC cron[187]: (CRON) INFO (pidfile fd = 3)
Aug 05 09:17:34 Rohit-PC cron[187]: (CRON) INFO (Running @reboot jobs)
Aug 05 10:17:01 Rohit-PC CRON[642]: pam_unix(cron:session): session opened >
Aug 05 10:17:01 Rohit-PC CRON[643]: (root) CMD (cd / && run-parts --report >
Aug 05 10:17:01 Rohit-PC CRON[642]: pam_unix(cron:session): session closed >
lines 1-40
[11]+  Stopped                 journalctl -u cron
Aug 05 11:17:00 Rohit-PC CRON[761]: pam_unix(cron:session): session opened >
lines 2-41^C
rohit@Rohit-PC:~$ journalctl -u cron -p err
-- No entries --
rohit@Rohit-PC:~$
```