# kubernetes-coreos-do 1.0.5

### Installation
Walkthrough for setup Kubernetes on CoreOS on DigitalOcean.

### Create Master Instance

Create a new droplet via DO interface, and choose following options
* Droplet Hostname: master
* Select Size: Any
* Select Region: Any with private networking support
* Available Settings: "Private Networking", "Enable User Data"
* Put cloud-config to user data textarea
* Select Image: CoreOS (stable)
* Choose you SSH key
* Press a "Create a Droplet" button

### Create Node Instance

Create a new droplet via DO interface, and choose following options
* Droplet Hostname: master
* Select Size: Any
* Select Region: Any with private networking support
* Available Settings: "Private Networking", "Enable User Data"
* Put cloud-config to user data textarea
* Set <master-private-ip> of master node in cloud config
* Select Image: CoreOS (stable)
* Choose you SSH key
* Press a "Create a Droplet" button

### Checking
* Connect to master `ssh core@%MASTER_DROPLET_EXTERNAL_IP%`
* fleetctl list-machines or kubectl get nodes 
