# fancontrol-hddtemp
Control fans with fancontrol by HDD/SSD temperature

# usage
* place fancontrol-hddtemp anywhere you like and make it executable
* run it `./fancontrol-hddtemp &` or use the servicefile and run it as systemd service
* find files with avg, max, 75th and 90th percentile temperatures
  * /srv/fancontrol-hddtemp/max
  * /srv/fancontrol-hddtemp/avg
  * /srv/fancontrol-hddtemp/pctl75
  * /srv/fancontrol-hddtemp/pctl90
* use one of these files as temperature sensor in fancontrol's config, e.g.:
  ```
  FCTEMPS=hwmon1/pwm1=/srv/fancontrol-hddtemp/max
  ```
* restart fancontrol
* profit
