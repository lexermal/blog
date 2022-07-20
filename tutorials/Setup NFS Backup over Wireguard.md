# Setup NFS Backup for Longhorn over Wireguard

Install wireguard with ```sudo apt-get install wireguard ```
Enable the kernel module with

```echo "wireguard" | sudo tee -a /etc/modules ```

Load the module without a reboot: ```sudo modprobe wireguard ```

Use my docker compose


docker network create wire_network --ip-range 172.19.150.0/24 --subnet 172.19.150.0/24




Use no quotes for the docker image NFS env variable or quote the whole variable

When the following error accures follow the following tutorial:
    mount: rpc_pipefs is write-protected, mounting read-only
    mount: cannot mount rpc_pipefs read-only
    could not open /proc/fs/nfs/exports for locking: errno 13 (Permission denied)


https://github.com/ehough/docker-nfs-server/blob/develop/doc/feature/apparmor.md

Install LXC when the following error accures: Could not open 'abstractions/lxc/container-base'

