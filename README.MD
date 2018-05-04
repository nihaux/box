Download you vpn *.ovpn files ex:"https://nordvpn.com/api/files/zip"
And unzip them in ./deluge/config/openvpn

check env variables available in docker-compose. Don't forget -E option to sudo to pass env var.

ex:
PGID=1000 PUID=1000 VPN_ENABLED=yes VPN_USER=YourVPNLoginHere VPN_PASS=YourVPNPasswordHere VPN_PROV=other sudo -E docker-compose up -d medusa deluge

