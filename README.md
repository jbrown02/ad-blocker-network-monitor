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

Then, navigate to: http://[IPADDRESS]/nagios (in this case, http://192.168.12.144/nagios
) to access the network moitor UI. If you don’t know your password, the following command can be used to change the password on the main user account, which is "Pi" for our purposes:

```
sudo htpasswd /usr/local/nagios/etc/htpasswd.users pi
```

The Pi Hole, on the other had, should be running as soon as the Pi is tured on as a default setting.  You can, however, use these commands to interface with the Pi Hole package:

```
sudo pihole status
sudo pihole enable
sudo pihole disable
```

You can access the Pi Hole admin portal at: http://[IPADDRESS]/admin (http://192.168.12.144/admin for this example)

Unlike with Nagios Core, however, you'll need to reinstall the Pi Hole if you misplace the password it generates for you. Make sure to write it down during the installation.

If your WiFi router isn’t cofigurable (T-Mobile), you will have to add the Pi Hole's IP address as a DNS server locally on your device instead of following the tutorials directly (they want you to edit the DNS settings on your router). This should be an available option in your network settings.

## Links

The following links are the tutorials that I used to set up my Pi Hole and my Nagios Core network monitor.

### Pi Hole:
https://pimylifeup.com/raspberry-pi-pi-hole/

https://core-electronics.com.au/guides/raspberry-pi/pi-hole-raspberry-pi/

### Nagios Core:
https://pimylifeup.com/raspberry-pi-nagios/

https://raspberrytips.com/nagios-raspberry-pi/
