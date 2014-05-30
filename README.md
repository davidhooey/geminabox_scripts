geminabox_scripts
=================

Includes a init.d script for Linux systems to auto start the rackup process. In this sample GemInABox is installed in the home directory of the rubygems users /home/rubygems.

##### 1. Install Ruby 1.9.3 using RVM as the rubygems user to avoid Ruby 2.0.0 issue https://github.com/geminabox/geminabox/issues/112.

##### 2. Edit the /home/rubygems/config.ru file to point to the full path of the data directory.
```
  Geminabox.data = "/home/rubygems/data"
```

##### 3. Install the init script (will be /etc/init.d/geminabox):
```
  sudo curl --output /etc/init.d/geminabox https://raw.github.com/davidhooey/geminabox_scripts/master/init.d/geminabox
  sudo chmod +x /etc/init.d/geminabox
```

##### 4. Edit the script changing the paths to match the geminabox installation.
```
  sudo vim /etc/init.d/geminabox
```

##### 5. Make geminabox start on boot:
```
  sudo update-rc.d geminabox defaults 21
```

##### 6. Control the service.
```
  sudo service geminabox [start|stop|status]
```
