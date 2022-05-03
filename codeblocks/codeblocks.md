```
#!/bin/bash
	
echo "hei maailma"
```
##
```
heimaailma:
  file.managed:
    - name: /usr/local/bin/heimaailma.sh
    - source: salt://heimaailma/heimaailma.sh
    - mode: 755
```
##
```
#!/bin/bash

echo ""
name=$(whoami)
echo "Heippa $name!"
echo ""
today=$(date "+%A %d. %Bta klo %T")
echo "Tänään on $today."
echo ""
ipaddress=$(hostname -i)
echo "IP-osoitteesi on $ipaddress."
echo ""
curl fi.wttr.in/Helsinki?0
```
##
```
whatsup:
  file.managed:
    - name: /usr/local/bin/whatsup.sh
    - source: salt://whatsup/whatsup.sh
    - mode: 755
```
##
```
hello:
  file.managed:
    - name: /usr/local/bin/hello.py
    - source: salt://python/hello.py
    - mode: 755
```
##
```
/usr/local/bin/:
  file.recurse:
    - source: salt://skriptit/
    - file_mode: 755
    - dir_mode: 755
```
