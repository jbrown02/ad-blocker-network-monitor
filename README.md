# CNE 350 Final - Justin Ellis, Spring 2023

## Running

You can run Nagios Core manually with the command:

```
sudo service nagios start
```

Alternatively, you can run it automatically on boot with:

```
sudo ln -s /etc/init.d/nagios /etc/rcS.d/S99nagios
```

Then, navigate to: http://[IPADDRESS]/nagios (in this case, http://[192.168.12.144]/nagios
) to access the network moitor UI. The Pi Hole, on the other had, will be running as soon as the Pi is tured on. If your WiFi router isn’t cofigurable (T-Mobile), you will have to add the Pi Hole's IP address as a DNS server locally on your device. This should be an available option in your network settings.

## Links

The following links are the tutorials that I used to set up my Pi Hole and my Nagios Core network monitor.

### Pi Hole:
https://pimylifeup.com/raspberry-pi-pi-hole/

https://core-electronics.com.au/guides/raspberry-pi/pi-hole-raspberry-pi/

### Nagios Core:
https://pimylifeup.com/raspberry-pi-nagios/

https://raspberrytips.com/nagios-raspberry-pi/
