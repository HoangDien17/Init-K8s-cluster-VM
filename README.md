REF: https://blog.devops.dev/how-to-setup-kubernetes-cluster-with-vagrant-e2c808795840

Make sure installed the dependencies packages
- Virtual box oracle version 7.1.4
    With chocolatey: choco install virtualbox
- Vagrant latest version
    With chocolatey: choco install vagrant

Install MetalLB on Kubernetes cluster running on VMWare VMs or bare metal server and nginx ingress:
https://blog.andreev.it/2023/10/install-metallb-on-kubernetes-cluster-running-on-vmware-vms-or-bare-metal-server/#Install_MetalLB


Attemption: make sure all nodes in K8s cluster have the same with the ip range that have defined in Metallb configuration
    Ex: if Nodes have ip: 10.0.0.x
    should define ip range: 10.0.0.50-10.0.0.60
