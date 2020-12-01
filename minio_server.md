## Minio Server OVA


- Download minio server OVA from [here](https://glasswall-sow-ova.s3.amazonaws.com/vms/Minio-Server/minio-server.ova?AWSAccessKeyId=AKIA3NUU5XSYVTP3BV6R&Signature=FZXLT6NqZyMMzOkkHEVD4T8K%2FzI%3D&Expires=1607569950)
- Open VMware > Open A Virtual Machine > Pick downloaded OVA file
- Before starting the VM, 
    - go to VM Settings > Add Network Adapter > Netowrk Connection: Host-only
    - make sure the first network adapter is set to **NAT**
- Start Minio Server VM
- Login (username: **glasswall**, password: **Gl@$$wall**)
- In the VM's terminal, run `ip a ` where you will find the IP address for `ens160`
- In your local hosts file (win: C:\Windows\System32\drivers\etc, on MAC/Linux: /etc/hosts), add:
    ```
    <VM IP_ADDRESS> minio.server
    ```
    **Example:** `192.168.66.128 minio.server`
- Open any browser and access [minio.server](http://minio.server)
- Login to Minio Server (username: **user**, password: **secret_password**)

