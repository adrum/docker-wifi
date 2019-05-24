# Docker Wifi

This use the wpa_supplicant package to generate a hashed psk for specific SSID to be used on any linux machine with wpa_supplicant installed. I'm using these specifically for Raspberry Pis.

`sudo docker run adrum/wifi wpa_passphrase "ssid" "password"`

Which generates the block below to be place in `/etc/wpa_supplicant/wpa_supplicant.conf`.

```
network={
	ssid="ssid"
	#psk="password"
	psk=44116ea881531996d8a23af58b376d70f196057429c258f529577a26e727ec1b
}
```
