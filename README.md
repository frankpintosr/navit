# Navit config for Raspberry Pi
This is a Raspberry PI customized navit configuration file using a 6m-gy-gps6m GPS module, and centered in Portland, Oregon USA.

> This configuration looks for a map file named "mapfile.bin" in /home/pi/maps/.  The second set of code will automatically rename it for you if the file is placed in the /home/pi/maps folder. 

Install Navit and Espeak packages and create folders for config and map files
```
sudo apt-get -y install navit espeak
mkdir ~/.navit
mkdir ~/maps
sudo wget -O ~/.navit/navit.xml https://raw.githubusercontent.com/frankpintosr/navit/master/navit.xml
```

Obtain your map file
```
Go to http://maps9.navit-project.org/ and download your map to /home/pi/maps
```

Rename the file to mapfile.bin
```
mv /home/pi/maps/*.bin /home/pi/maps/mapfile.bin
```

Add Navit to the desktop start menu
```
sudo wget -O /usr/share/applications/navit.desktop https://raw.githubusercontent.com/frankpintosr/navit/master/navit.desktop
```

Your all set!  Run Navit from the command line interface and test
```
navit
```
