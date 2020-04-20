# StrongSwan IKEv2 VPN setup

### Deploy with Pre Shared Key auth

This script would uuidgen a PSK and print it out to console, where you can copy and hit enter to continue.

After you `ssh your_vpn_machine`, just run this: 
```
curl -L https://raw.githubusercontent.com/quyendang/ikev2_vpn/master/ikev2-deploy-psk.sh -o ~/deploy.sh && chmod +x ~/deploy.sh && ~/deploy.sh
```

### Deploy with cert / username-password auth

The .pem files would be in `~/vpn-certs/`
<br>You can add your users to `/etc/ipsec.secrets`, make sure to reboot afterwards

After you `ssh your_vpn_machine`, just run this: 
```
curl -L https://raw.githubusercontent.com/quyendang/ikev2_vpn/master/ikev2-deploy-certs.sh -o ~/deploy.sh && chmod +x ~/deploy.sh && ~/deploy.sh
```