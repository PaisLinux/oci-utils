# OCI Certificate management with letsencrypt

1. Copy oci-certificate to `/usr/local/sbin/`
1. Create directory `/usr/local/etc/certs/`
1. Install oci-certificate.conf in `/usr/local/etc/certs/`
1. Customize oci-certificate.conf and rename it to suit your needs
1. Run acme.sh as in bellow example
```
acme.sh --install-cert -d whatever.example.com \
        --cert-file /usr/local/etc/certs/whatever.example.com/whatever.example.com.cer \
        --key-file /usr/local/etc/certs/whatever.example.com/whatever.example.com.key \
        --ca-file /usr/local/etc/certs/whatever.example.com/ca.cer \
        --reloadcmd "/usr/local/sbin/oci-certificate /usr/local/etc/certs/whatever.example.conf"
