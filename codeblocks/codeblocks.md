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
echo "Heippa!"
whoami
echo ""
echo "Tänään on"
date "+%A %d. %Bta klo %T"
echo ""
echo "IP-osoitteesi on:"
hostname -i
echo ""
curl fi.wttr.in/Helsinki?0
```
