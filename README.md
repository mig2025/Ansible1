Первые шаги с Ansible
-------
Рабочее место => Open Suse 15.6
Virtual Box Version => 7.0
------
Проблемы:

конфиг ["192.168.11.150",  2, "255.255.255.0", "mynet"] => не работает:

ping: 

mig@localhost:~/Ansible> ping 192.168.11.150
PING 192.168.11.150 (192.168.11.150) 56(84) Bytes an Daten.

конфиг ["192.168.11.150"] => ошибка:

The IP address configured for the host-only network is not within the
allowed ranges.

Address: 192.168.11.150
Ranges: 192.168.56.0/21

конфиг ["192.168.56.150"] => работает:

ping:

PING 192.168.56.150 (192.168.56.150) 56(84) Bytes an Daten.
64 Bytes von 192.168.56.150: icmp_seq=1 ttl=64 Zeit=1.85 ms
64 Bytes von 192.168.56.150: icmp_seq=2 ttl=64 Zeit=0.743 ms
64 Bytes von 192.168.56.150: icmp_seq=3 ttl=64 Zeit=5.97 ms
64 Bytes von 192.168.56.150: icmp_seq=4 ttl=64 Zeit=1.01 ms
-----
curl http://192.168.56.150:8080

<h1>Welcome to nginx!</h1># Ansible1
