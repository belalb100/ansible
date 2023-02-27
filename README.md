
# IaC

### What is infrastructure as code?
Infrastructure as code (IaC) is a way of managing computer infrastructure, like servers and networks, by using machine-readable files to define and automate the setup and configuration of these resources. Instead of manually configuring hardware devices, IaC allows developers to use code to define their infrastructure, which can be version-controlled, tested, and deployed like software code. This makes infrastructure deployment faster, more reliable, and easier to scale up or down as needed. Popular tools for implementing IaC include Terraform, Ansible, Puppet, Chef, and CloudFormation.

### What coding languages are used?

There is no one specific coding language used for Infrastructure as Code (IaC). Instead, IaC can be implemented using a variety of programming languages, configuration files, or scripts depending on the tool being used.

Some popular programming languages used for IaC include:

HashiCorp Configuration Language (HCL) - used in HashiCorp's Terraform
YAML - used in Ansible and Kubernetes
JSON - used in AWS CloudFormation
Ruby - used in Chef


### Terraform and Ansible:

Terraform and Ansible are two popular Infrastructure-as-Code (IaC) tools that are used to manage and automate IT infrastructure. 

Terraform is a tool for building, changing, and versioning infrastructure safely and efficiently.
Terraform allows you to create infrastructure by defining resources, such as servers, networks, and storage, in code. It uses a state file to track the current state of the infrastructure and manages dependencies between resources to ensure that they are created and updated in the correct order. Terraform is ideal for provisioning and managing infrastructure that will be deployed to the cloud.

Ansible, on the other hand, is a tool for automating the configuration and management of systems. It provides a simple, human-readable language for defining tasks that can be executed on remote hosts. Ansible uses an agentless architecture, which means that it does not require any software to be installed on the managed hosts. 



### Why Use Infrastructure as Code?
In the early 2000s, managing an IT infrastructure was a highly manual and complex process for big companies. Experts had to physically install and configure servers and other types of hardware, which was a slow, inconsistent and costly way to manage IT. 

With IaC, there’s no need for this kind of manual configuration. Instead, DevOps teams can automatically manage, monitor and provision resources. By using IaC, the provisioning code becomes easy to edit, copy and distribute.

Notice that, like any other software development project, developers must maintain version control, test iterations and limit deployments. So, even though IaC is a great approach for automating complex manual processes, it also includes new tools and overhead for the developers.





# Ansible

### Creating an environment for Ansible using Vagrant

Firstly we create three virtual machines as shown in the diagram 1 for our ansible controller and the other 2 for our app and db VM.

Inside directory with vagrantfile Vagrant up we do this in GitBash
then
`Vagrant ssh controller` and then `Vagrant ssh app` and then `Vagrant ssh db`whilst running update and upgrade in all these VM afterwards we go back the the controller VM and from there we run the following in order:

`sudo apt-get install software-properties-common`
then 
`sudo apt-add-repository ppa:ansible/ansible`
then
`sudo apt-get install ansible -y`

next we check the version of ansible using `sudo ansible --version`

next we need to test ansible controller and check does it have everything to communicate with the different nodes as shown in the image.
we then `cd /etc` then `cd /ansible` 
Now we need to see if we can communicate with the two other machines APP and DB by using `ssh vagrant@192.168.33.10`
when we do this the controller will send a request to ssh in, we will need to do this using a password but it will be denied as there is no key nor does the other node expect anything.






![Alt text](images/ansible.png)



