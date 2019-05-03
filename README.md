# SOII
# Comandos de consola

### date -u +"%Y-%m-%d
_Muestra la fecha actual con el formato indicado donde ***%Y*** indica el año, ***%m*** el mes y ***%d*** el dia._
```
thechrisvazquez@disimil:~$ date -u +"%Y-%m-%d"
2019-05-03
```

### which $PROGRAMA
_Muestra la ruta absoluta de un programa instalado._
```
thechrisvazquez@disimil:~$ which firefox
/usr/bin/firefox
```

### ps
_Arroja una lista en la que muestra los procesos que estan ejecutandose en el sistema._
```
thechrisvazquez@disimil:~$ ps
  PID TTY          TIME CMD
 2037 pts/0    00:00:00 bash
 2080 pts/0    00:00:00 ps
```
### history
_Muestra una lista completa de todo el historial de comandos ejecutados en la consola._
```
thechrisvazquez@disimil:~$ history
    1  su
    2  exit
    3  su
    4  exit
    5  cd  /usr/lib/jvm/
    6  cd java-11-oracle/
    7  exit
```
### less
_Vizualiza el contenido de un archivo con permisos unicamente de solo lectura._
```
thechrisvazquez@disimil:~$ history | less
```
### who
_Muestra los usuarios que estan activos._
```
thechrisvazquez@disimil:~$ who
thechrisvazquez tty2         2019-05-02 23:05 (:0)
```
### uptime
_Muestra el tiempo que lleva activo el equipo y el numero de usuarios que han interctuado._
```
thechrisvazquez@disimil:~$ uptime
 23:43:49 up 38 min,  1 user,  load average: 0.09, 0.18, 0.18
```
### telnet $IP $PORT
_Indica si esta activo o no el puerto indicado, siendo ***$IP*** una direccion ip real y ***$PORT*** el puerto a seleccionar.(Para salir ***Ctrl+] y Ctrl+d*** )_
```
thechrisvazquez@disimil:~$ telnet 127.0.0.1 21
Trying 127.0.0.1...
Connected to 127.0.0.1.
Escape character is '^]'.
220 ProFTPD 1.3.4c Server (ProFTPD) [::ffff:127.0.0.1]
^]
telnet> Connection closed.
```
### sudo -c $COMANDO
_Se ejecuta un comando en modo usuario root, siendo ***$COMANDO*** la instruccion a ejecutar._
```
thechrisvazquez@disimil:~$ su -c apt install elPrograma.sh
```
### sudo $COMANDO
_Se ejecuta un comando en modo usuario superusuario, siendo ***$COMANDO*** la instruccion a ejecutar._
```
thechrisvazquez@disimil:~$ su -c apt update
```
### nmap -Pn $IP
_Muestra los puertos que estan activos, siendo ***$IP*** una direccion de ip real._
```
thechrisvazquez@disimil:~$ nmap -Pn 127.0.0.1
Starting Nmap 7.40 ( https://nmap.org ) at 2019-05-03 00:02 CDT
Nmap scan report for localhost (127.0.0.1)
Host is up (0.00032s latency).
Not shown: 996 closed ports
PORT     STATE SERVICE
21/tcp   open  ftp
80/tcp   open  http
443/tcp  open  https
3306/tcp open  mysql
Nmap done: 1 IP address (1 host up) scanned in 0.08 seconds
```
### traceroute $IP
_Crea una prueba de conexion hacia la ip indicada, siendo ***$IP*** una direccion de ip real._
```
thechrisvazquez@disimil:~$ traceroute 127.0.0.1
traceroute to 127.0.0.1 (127.0.0.1), 30 hops max, 60 byte packets
 1  localhost (127.0.0.1)  0.063 ms  0.010 ms  0.009 ms
```
### bc
_Se ejecuta un editor de operaciones algebraicas.(Para salir ***Ctrl+d***)_
```
thechrisvazquez@disimil:~$ bc
bc 1.06.95
Copyright 1991-1994, 1997, 1998, 2000, 2004, 2006 Free Software Foundation, Inc.
This is free software with ABSOLUTELY NO WARRANTY.
For details type `warranty'. 
(10+5)
15
```
### ping $IP
_Ejecuta una prueba de conexion, siendo  ***$IP*** una ip real.(Para finalizar la tarea ***Ctrl+c***)_
```
thechrisvazquez@disimil:~$ ping www.google.com
PING www.google.com (172.217.15.4) 56(84) bytes of data.
64 bytes from qro01s18-in-f4.1e100.net (172.217.15.4): icmp_seq=1 ttl=57 time=13.7 ms
64 bytes from qro01s18-in-f4.1e100.net (172.217.15.4): icmp_seq=2 ttl=57 time=22.4 ms
^X64 bytes from qro01s18-in-f4.1e100.net (172.217.15.4): icmp_seq=3 ttl=57 time=39.7 ms
64 bytes from qro01s18-in-f4.1e100.net (172.217.15.4): icmp_seq=4 ttl=57 time=32.4 ms
^C
--- www.google.com ping statistics ---
4 packets transmitted, 4 received, 0% packet loss, time 3001ms
rtt min/avg/max/mdev = 13.789/27.117/39.775/9.856 ms
```
### " | "
_El simbolo ***" |"  pipe***, sirve para enviar un argumento hacia una instruccion._
```
thechrisvazquez@disimil:~$ history | less
```
### " < "
_Extrae el contenido de un archivo._
```
thechrisvazquez@disimil:~$ less < archivo.txt
```
### top
_Muestra un listado de los procesos que se va actualizando dependiendo que proceso esté abarcando mayor cantidad de memoria._
```
top - 00:20:43 up  1:15,  1 user,  load average: 0.08, 0.17, 0.20
Tasks: 200 total,   1 running, 199 sleeping,   0 stopped,   0 zombie
%Cpu(s):  1.2 us,  2.4 sy,  0.0 ni, 96.4 id,  0.0 wa,  0.0 hi,  0.0 si,  0.0 st
KiB Mem :  3841564 total,   921648 free,  1597800 used,  1322116 buff/cache
KiB Swap:   975868 total,   975868 free,        0 used.  1810108 avail Mem 

  PID USER      PR  NI    VIRT    RES    SHR S  %CPU %MEM     TIME+ COMMAND     
 3410 thechri+  20   0   44904   3744   3084 R   9.5  0.1   0:00.13 top         
 1085 thechri+  20   0  415748  74692  41240 S   4.8  1.9   1:32.28 Xorg        
 1171 thechri+  20   0 1937564 204404  62688 S   4.8  5.3   1:53.67 gnome-shell 
    1 root      20   0  204624   6956   5236 S   0.0  0.2   0:01.03 systemd     
    2 root      20   0       0      0      0 S   0.0  0.0   0:00.00 kthreadd    
    3 root      20   0       0      0      0 S   0.0  0.0   0:00.02 ksoftirqd/0 
    5 root       0 -20       0      0      0 S   0.0  0.0   0:00.00 kworker/0:+ 
    6 root      20   0       0      0      0 S   0.0  0.0   0:01.51 kworker/u1+ 
    7 root      20   0       0      0      0 S   0.0  0.0   0:00.78 rcu_sched   
    8 root      20   0       0      0      0 S   0.0  0.0   0:00.00 rcu_bh      
    9 root      rt   0       0      0      0 S   0.0  0.0   0:00.00 migration/0 
   10 root       0 -20       0      0      0 S   0.0  0.0   0:00.00 lru-add-dr+ 
   11 root      rt   0       0      0      0 S   0.0  0.0   0:00.00 watchdog/0  
   12 root      20   0       0      0      0 S   0.0  0.0   0:00.00 cpuhp/0     
   13 root      20   0       0      0      0 S   0.0  0.0   0:00.00 cpuhp/1     
   14 root      rt   0       0      0      0 S   0.0  0.0   0:00.00 watchdog/1  
   15 root      rt   0       0      0      0 S   0.0  0.0   0:00.00 migration/1 
```
### sleep $N
_Ejecuta un descanso en  las instrucciones dependiendo la cantidad asignada, siendo ***$N*** el numero de segundos a descansar._
```
thechrisvazquez@disimil:~$ sleep 10
```


###### _Vazquez Valdivia Christian Alan_
