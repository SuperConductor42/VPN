
# Windows

## Installation and Setup

1. Download and install [OpenVPN client](https://swupdate.openvpn.org/community/releases/openvpn-install-2.4.6-I602.exe).
2. Run the newly installed OpenVPN GUI desktop app. (A tray icon should appear in the taskbar after opening). 
3. Download the FVPN [config file](/downloads/FVPN.ovpn).
4. Import the 'FVPN.ovpn' config file into the OpenVPN client (Right click on the tray icon and select 'Import File').
5. Download [this batch script](/downloads/FVPN_tunnel.bat) and place it in an accessible location (perhaps your desktop).

## Connect

1. Run the batch file and enter the password when prompted. (Password Hint: I'm actually pretty good at it).
2. Open the OpenVPN client. (Double click the tray icon in the taskbar)
3. Enter your details into the login prompt. Contact me if you don't have them.
4. Wait about 30 seconds for the connect procedure to complete.
5. You should hopefully be connected to the VPN :)

## Disconnect

1. Double click the tray icon in your taskbar and click 'Disconnect'
2. The running command prompt window should automatically close. If not, you can close it yourself.

<hr>

# Mac

## Installation and Setup

1. Download and install [tunnelblick](https://tunnelblick.net/release/Latest_Tunnelblick_Stable.dmg).
2. After installation tunnelblick should start and ask for a configuration file.
3. Select 'I have configuration files' and click ok.
4. Click the tunnelblick icon in your menubar and select 'VPN Details'
5. Download the FVPN [config file](/downloads/FVPN.ovpn).
6. Drag that file (FVPN.ovpn) into the tunnelblick VPN Details window and follow the on-screen instructions.
7. Once installed you can now close the details window.
8. Download [this command file](/downloads/FVPN_tunnel.command).
9. Open Terminal and enter the command `chmod a+x ~/Downloads/FVPN_tunnel.command && exit`
10. Move that file (FVPN_tunnel.command) to an accessible location (Perhaps your desktop).

## Connect

1. Run the FVPN_tunnel.command file and enter the password when prompted. (Password Hint: I'm actually pretty good at it).
2. Click on the tunnelblick icon in the menubar and select 'Connect FVPN'
3. Enter your details into the login prompt. Contact me if you don't have them.
4. Wait about 30 seconds for the connect procedure to complete.
5. You should be connected to the VPN. :)

## Disconnect

1. Click the tunnelblick icon in the menubar and select 'Disconnect FVPN'
2. You can now close the FVPN_tunnel.command terminal window.

<hr>

# Extra

This VPN uses an SSH tunnel to disguise it's traffic in such a way that a DPI (deep packet inspection) firewall can't detect it. 
This is why you need to run the FVPN_tunnel script before connecting to the VPN.
If you wish to connect directly to the VPN (without having to run the FVPN_tunnel script), you can do so with this [config file](/downloads/FVPN Direct.ovpn).
Just install the file as usual into your OpenVPN clinet.
Keep in mind that this configuration is unlikely to work behind filtered networks.
