muninlite
=========

Muninlite for EdgeOS

At the moment there is no packge available to install Munin-Node on EdgeOS devices. Fortunately you can use muninlite (http://sourceforge.net/projects/muninlite/). This script extends the QNAP-custom verson by at https://github.com/gpkvt/muninlite to make some small changes.

Installation
============

1. Copy the Script to ```/config/scripts/munin-node```

2. Create a new non-administrator user called ```munin``` either in the CLI or Web UI

3. Generate an ssh key for the user running Munin on your master server (if you haven't done so already) and add the public key to the user created in step #2

4. Add the node config to the ```munin.conf``` on the Munin master:
```
[my-edge-os-device]
    address ssh://USER@HOST /config/scripts/munin-node.sh
    use_node_name yes

```

