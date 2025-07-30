Create torrc with no .txt in same folder with tor.exe

```
SocksPort 9050

HiddenServiceDir E:\Tor\TorExpertBundle\tor\TorHiddenService1 #You must create a folder before running.
HiddenServiceVersion 3
HiddenServicePort 80 127.0.0.1:8080

HiddenServiceDir E:\Tor\TorExpertBundle\tor\TorHiddenService2 #You must create a folder before running.
HiddenServiceVersion 3
HiddenServicePort 25565 127.0.0.1:25565

DataDirectory E:\Tor\TorExpertBundle\Data

Log notice stdout
```

tor.exe -f torrc

netstat -ano | findstr :9050

tasklist /FI "PID eq <PID>"

curl https://check.torproject.org/

netsh trace start capture=yes tracefile=c:\temp\nettrace.etl