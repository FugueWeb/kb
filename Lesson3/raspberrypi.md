## Setup

* [Raspberry Pi Projects](https://projects.raspberrypi.org/en/projects)

## IOTStack

IOTstack is a builder for docker-compose to easily make and maintain IoT stacks on the Raspberry Pi.

* [Docs](https://github.com/SensorsIot/IOTstack)
* [GitHub](https://github.com/SensorsIot/IOTstack)
* [DropBox Uploader](https://github.com/andreafabrizi/Dropbox-Uploader) - Backup `volumes` folder where data is stored. Needs API key added during installation

## Backups

* `crontab -e`
* `* 23 * * * sudo ~/Path_to_IOTStack/scripts/docker_backup.sh >/dev/null 2>&1`
    * Starts backup at 11pm

## Pi VPN

* [PiVPN : How to Run a VPN Server on a $35 Raspberry Pi!](https://www.youtube.com/watch?v=15VjDVCISj0)
* [Accessing your device from the internet](https://sensorsiot.github.io/IOTstack/Accessing-your-Device-from-the-internet/)
* `crontab -e`
* `*/5 * * * ~/Path_to_IOTStack/duck/duck.sh >/dev/null 2>&1`
    * Updates IP address every 5 minutes, used with Duck DNS
* Copy key to device
* [No-IP](https://noip.com)

## Remote Access on Android
* VNC Viewer
* SSH Client - Termux
* Network Scanner

## Resources

* [EVERYONE needs to learn LINUX - ft. Raspberry Pi 4](https://www.youtube.com/watch?v=l9YxTXDiiFY) | Video
* [Raspberry Pi Server based on Docker, with VPN, Dropbox backup, Influx, Grafana, etc.](https://www.youtube.com/watch?v=a6mjt8tWUws) | Video
