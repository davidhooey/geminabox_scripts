geminabox_scripts
=================

Includes a init.d script for Linux systems to auto start the rackup process.

### 1. Install the init script (will be /etc/init.d/geminabox):
```
  sudo curl --output /etc/init.d/geminabox https://raw.github.com/davidhooey/geminabox_scripts/master/init.d/geminabox
  sudo chmod +x /etc/init.d/geminabox
```

### 2. Edit the script changing the paths to match the geminabox installation.
```
  sudo vim /etc/init.d/geminabox
```

### 3. Make geminabox start on boot:
```
  sudo update-rc.d geminabox defaults 21
```

### 4. Edit the config.ru file to point to the full path of the data directory.
```
  Geminabox.data = "/home/rubygems/data"
```
