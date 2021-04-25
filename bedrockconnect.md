# Joining via Console

<!--ts-->
   * [About](#About)
   * [DNS Method](#DNS-Method)
      * [XBox](#XBox)
      * [PS4](#PS4)
      * [Switch](#Switch)
      * [FireTV](#FireTV)
   * [Hosting a Local BedrockConnect Instance](#Hosting-a-Local-BedrockConnect-Instance)
<!--te-->

## About
[BedrockConnect](https://github.com/Pugmatt/BedrockConnect) works by essentially initiating a man-in-the middle attack on the domain of the featured servers. Basically, this means that when the device attempts to look up the IP of, say, Hypixel, from its domain, BedrockConnect's DNS server will instead return the IP of the BedrockConnect server list server, which will allow you to join IF.

## DNS Method
- Change the primary DNS server on your device to 104.238.130.180 and the secondary DNS server to 1.1.1.1
- If you are on PS4, use 173.82.100.84 as your primary DNS
- If you cannot connect, refer to the [troubleshooting guide](https://github.com/Pugmatt/BedrockConnect/wiki/Troubleshooting)

### XBox
1. Open the Network screen by pressing the Xbox button (Xbox logo) and then selecting `Settings` > `Network` > `Network Settings`.
2. Select `Advanced Settings`.
3. Select `DNS Settings`.
4. Select `Manual`.
5. Set `Primary DNS` to: `104.238.130.180`.
6. Set Secondary DNS to: `1.1.1.1`.
7. When you are finished, you will be shown a confirmation screen. Press the B button to save.

### PS4
1. Select `Settings`.
2. Select `Network`.
3. Select `Set Up Internet Connection`.
4. Select `Wifi` or `LAN` (depending on how you connect to the internet).
5. Select `Custom`.
6. Toggle `IP Address Settings` to `Automatic`.
7. Toggle `DHCP Host Name` to `Do Not Specify`.
8. Toggle `DNS Settings` to `Manual`.
9. Set `Primary DNS` to: `173.82.100.84`.
10. Set `Secondary DNS` to: `1.1.1.1`.
12. Toggle `MTU Settings` to `Automatic`.
13. Toggle `Proxy Server` to `Do Not Use`.

### Switch
1. Go to the home menu and choose `System Settings` (wrench icon).
2. Select `Internet Settings` > `Connection Settings`.
3. Select your internet connection and then select `Change Settings`.
4. Select `Change DNS`.
5. Set `Auto-Obtain DNS` to `No`.
6. Select `Detailed Setup`.
7. Set `Primary DNS` to: `104.238.130.180`.
8. Set Secondary DNS to: `1.1.1.1`.
9. Select `Save` then `OK`.

### FireTV
1. Go to `Settings` > `My Fire TV` > `About` > `Network` and note down the listed information.
2. Go to `Settings` > `Network` and select your WiFi network. 
3. Click the remote menu button (☰) to forget the network.
4. Click on the connection again and enter the network password you noted earlier (SSID).
5. Select `Advanced`.
6. Enter the `IP Address` you noted earlier.
7. Enter the `Gateway` IP you noted earlier.
8. Enter the `Network Prefix Length` based on the subnet mask you noted earlier.
  - For `255.255.255.0` enter `32`.
  - For `255.255.0.0` enter `64`.
  - For any other value, enter your subnet mask into this [tool](https://www.subnet-calculator.com/cidr.php) and use the output.
9. Set `DNS 1` to `104.238.130.180`.
10. Set `DNS 2` to `1.1.1.1`.

## Hosting a Local BedrockConnect Instance
- If you run into trouble with the DNS method, consider hosting a local instance of BedrockConnect on an availible device
- Download the [latest release](https://github.com/Pugmatt/BedrockConnect/releases)
- Assuming you are cd to the directory containing the jar, run:
  - `java -jar BedrockConnect-1.0-SNAPSHOT.jar nodb=true`
- On Windows, command prompt may not use a current 64-bit JRE, so you will need to fix this by referring to this [guide](https://www.happycoders.eu/java/how-to-switch-multiple-java-versions-windows/)
- Once running, connect via the friends tab
