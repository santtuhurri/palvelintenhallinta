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
