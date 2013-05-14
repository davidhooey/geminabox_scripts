geminabox_scripts
=================

Includes a init.d script for Linux systems to auto start the rackup process. In this sample GemInABox is installed in the home directory of the rubygems users /home/rubygems.

### 1. Edit the /home/rubygems/config.ru file to point to the full path of the data directory.
```
  Geminabox.data = "/home/rubygems/data"
```

### 2. Install the init script (will be /etc/init.d/geminabox):
```
  sudo curl --output /etc/init.d/geminabox https://raw.github.com/davidhooey/geminabox_scripts/master/init.d/geminabox
  sudo chmod +x /etc/init.d/geminabox
```

### 3. Edit the script changing the paths to match the geminabox installation.
```
  sudo vim /etc/init.d/geminabox
```

### 4. Make geminabox start on boot:
```
  sudo update-rc.d geminabox defaults 21
```

### 5. Control the service.
```
  sudo service geminabox [start|stop|status]
```
