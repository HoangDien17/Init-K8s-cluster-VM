REF: https://blog.devops.dev/how-to-setup-kubernetes-cluster-with-vagrant-e2c808795840

Make sure installed the dependencies packages
- Virtual box oracle version 7.1.4
    With chocolatey: choco install virtualbox
- Vagrant latest version
    With chocolatey: choco install vagrant

Install MetalLB on Kubernetes cluster running on VMWare VMs or bare metal server and nginx ingress:
https://blog.andreev.it/2023/10/install-metallb-on-kubernetes-cluster-running-on-vmware-vms-or-bare-metal-server/#Install_MetalLB

Another example: 
https://github.com/lacoski/kubernetes-note/blob/main/docs/setup/install-metallb.md

Attemption: make sure all nodes in K8s cluster have the same with the ip range that have defined in Metallb configuration
    Ex: if Nodes have ip: 10.0.0.x
    should define ip range: 10.0.0.50-10.0.0.60

To access cluster from local machines, need to copy .kube/config from master node to ~/.kube/cofig
- Find the Vagrant private key location:
    vagrant ssh-config
- Use scp with the private key:
    scp -i /path/to/private/key -P 2222 vagrant@127.0.0.1:/home/vagrant/.kube/config ~/.kube/config
- In local, set up env variable: 
    export KUBECONFIG=~/.kube/config
