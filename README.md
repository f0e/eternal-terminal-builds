# eternal terminal builds

Unofficial compiled binaries for [Eternal Terminal](https://github.com/MisterTea/EternalTerminal) automatically generated for each commit.

I use this on my Unraid server as part of an "At First Array Start Only" userscript:

```bash
#!/bin/bash

# download et binaries
wget -O /tmp/et.tar.gz https://github.com/f0e/eternal-terminal-builds/releases/latest/download/et-linux-amd64.tar.gz
tar -xzf /tmp/et.tar.gz -C /usr/bin --strip-components=1
rm -f /tmp/et.tar.gz

# run etserver in the background
/usr/bin/etserver &

echo "Eternal Terminal server started in the background."
```
