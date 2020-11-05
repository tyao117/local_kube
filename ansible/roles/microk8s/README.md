# MicroK8s Installation

This role is used to install microk8s on raspberry-pi

Links:
- https://dev.to/musabhusaini/remote-development-with-multi-node-microk8s-cluster-and-scaffold-4o1d

Errors:

    Nov 05 02:54:45 kubeworker2 microk8s.daemon-kubelet[22455]: + export PATH=/snap/microk8s/1752/usr/sbin:/snap/microk8s/1752/usr/bin:/snap/microk8s/1752/sbin:/snap/microk8s/1752/bin:/>
    Nov 05 02:54:45 kubeworker2 microk8s.daemon-kubelet[22455]: + PATH=/snap/microk8s/1752/usr/sbin:/snap/microk8s/1752/usr/bin:/snap/microk8s/1752/sbin:/snap/microk8s/1752/bin:/usr/loc>
    Nov 05 02:54:45 kubeworker2 microk8s.daemon-kubelet[22502]: ++ /snap/microk8s/1752/bin/uname -m
    Nov 05 02:54:45 kubeworker2 microk8s.daemon-kubelet[22455]: + ARCH=aarch64
    Nov 05 02:54:45 kubeworker2 microk8s.daemon-kubelet[22455]: + export LD_LIBRARY_PATH=:/snap/microk8s/1752/lib:/snap/microk8s/1752/usr/lib:/snap/microk8s/1752/lib/aarch64-linux-gnu:/>
    Nov 05 02:54:45 kubeworker2 microk8s.daemon-kubelet[22455]: + LD_LIBRARY_PATH=:/snap/microk8s/1752/lib:/snap/microk8s/1752/usr/lib:/snap/microk8s/1752/lib/aarch64-linux-gnu:/snap/mi>
    Nov 05 02:54:45 kubeworker2 microk8s.daemon-kubelet[22455]: + export LD_LIBRARY_PATH=/var/lib/snapd/lib/gl:/var/lib/snapd/lib/gl32:/var/lib/snapd/void::/snap/microk8s/1752/lib:/snap>
    Nov 05 02:54:45 kubeworker2 microk8s.daemon-kubelet[22455]: + LD_LIBRARY_PATH=/var/lib/snapd/lib/gl:/var/lib/snapd/lib/gl32:/var/lib/snapd/void::/snap/microk8s/1752/lib:/snap/microk>
    Nov 05 02:54:45 kubeworker2 microk8s.daemon-kubelet[22455]: + source /snap/microk8s/1752/actions/common/utils.sh
    Nov 05 02:54:45 kubeworker2 microk8s.daemon-kubelet[22455]: + app=kubelet
    Nov 05 02:54:45 kubeworker2 microk8s.daemon-kubelet[22455]: + '[' -e /var/snap/microk8s/1752/var/lock/clustered.lock ']'
    Nov 05 02:54:45 kubeworker2 microk8s.daemon-kubelet[22455]: + '[' kubelet = kubelet ']'
    Nov 05 02:54:45 kubeworker2 microk8s.daemon-kubelet[22517]: ++ tr = ' '
    Nov 05 02:54:45 kubeworker2 microk8s.daemon-kubelet[22519]: ++ gawk '{print $2}'
    Nov 05 02:54:45 kubeworker2 microk8s.daemon-kubelet[22514]: ++ grep pod-cidr
    Nov 05 02:54:45 kubeworker2 microk8s.daemon-kubelet[22513]: ++ cat /var/snap/microk8s/1752/args/kubelet
    Nov 05 02:54:46 kubeworker2 microk8s.daemon-kubelet[22455]: + pod_cidr=
    Nov 05 02:54:46 kubeworker2 microk8s.daemon-kubelet[22455]: + '[' -z '' ']'
    Nov 05 02:54:46 kubeworker2 microk8s.daemon-kubelet[22723]: ++ jq .Network /var/snap/microk8s/1752/args/flannel-network-mgr-config
    Nov 05 02:54:46 kubeworker2 microk8s.daemon-kubelet[22724]: ++ tr -d '\"'
    Nov 05 02:54:47 kubeworker2 microk8s.daemon-kubelet[22455]: + pod_cidr=10.1.0.0/16
    Nov 05 02:54:47 kubeworker2 microk8s.daemon-kubelet[22455]: + '[' -z 10.1.0.0/16 ']'
    Nov 05 02:54:47 kubeworker2 microk8s.daemon-kubelet[22455]: + iptables -C FORWARD -s 10.1.0.0/16 -m comment --comment 'generated for MicroK8s pods' -j ACCEPT
    Nov 05 02:54:47 kubeworker2 microk8s.daemon-kubelet[22769]: iptables: Bad rule (does a matching rule exist in that chain?).
    Nov 05 02:54:47 kubeworker2 microk8s.daemon-kubelet[22455]: + iptables -t filter -A FORWARD -s 10.1.0.0/16 -m comment --comment 'generated for MicroK8s pods' -j ACCEPT
    Nov 05 02:54:47 kubeworker2 microk8s.daemon-kubelet[22455]: + iptables -t filter -A FORWARD -d 10.1.0.0/16 -m comment --comment 'generated for MicroK8s pods' -j ACCEPT
    Nov 05 02:54:47 kubeworker2 microk8s.daemon-kubelet[22455]: + grep -e '--address ' /var/snap/microk8s/1752/args/containerd
    Nov 05 02:54:47 kubeworker2 microk8s.daemon-kubelet[22777]: ++ grep -e '--address ' /var/snap/microk8s/1752/args/containerd
