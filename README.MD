sudo snap install docker
sudo curl -L https://github.com/docker/compose/releases/download/1.21.0/docker-compose-$(uname -s)-$(uname -m) -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose


Download you vpn *.ovpn files ex:"https://nordvpn.com/api/files/zip"
And unzip them in ./deluge/config/openvpn

wget https://nordvpn.com/api/files/zip && unzip ./zip -d ./deluge/config/openvpn && rm ./zip

check env variables available in docker-compose. Don't forget -E option to sudo to pass env var.

ex:
PGID=1000 PUID=1000 VPN_ENABLED=yes VPN_USER=YourVPNLoginHere VPN_PASS=YourVPNPasswordHere VPN_PROV=other sudo -E docker-compose up -d medusa deluge

