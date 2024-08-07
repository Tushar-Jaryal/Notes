- Ansible is an open source automation and orchestration tool for software provisioning, configuration management, and software deployment. Ansible can easily run and configure Unix-like systems as well as Windows systems to provide infrastructure as code. It contains its own declarative programming language for system configuration and management.
- Ansible is popular for its simplicity of installation, ease of use in what concerns the connectivity to clients, its lack of agent for Ansible clients and the multitude of skills. It functions by connecting via SSH to the clients, so it doesn't need a special agent on the client-side, and by pushing modules to the clients, the modules are then executed locally on the client-side and the output is pushed back to the Ansible server.
- Since it uses SSH, it can very easily connect to clients using SSH-Keys, simplifying through the whole process. Client details, like hostnames or IP addresses and SSH ports, are stored in files called inventory files. Once you have created an inventory file and populated it, ansible can use it.

## Why use Ansible?

Here are some important pros/benefits of using Ansible
- One of the most significant advantages of Ansible is that it is free to use by everyone.
- It does not need any special system administrator skills to install and use Ansible, and the official documentation is very comprehensive.
- Its modularity regarding plugins, modules, inventories, and playbooks make Ansible the perfect companion to orchestrate large environments.
- Ansible is very lightweight and consistent, and no constraints regarding the operating system or underlying hardware are present.
- It is also very secure due to its agent less capabilities and due to the use of OpenSSH security features.
- Another advantage that encourages the adoption of Ansible is its smooth learning curve determined by the comprehensive documentation and easy to learn structure and configuration.

## History of Ansible
- In February 2012 the ansible project began. It was first developed by Michael DeHaan, the creator of Cobbler and Func, Fedora Unified Network Controller.
- Initially called AnsibleWorks Inc, the company funding the ansible tool was accquired in 2015 by RedHat and later on, along with RedHat, moved under the umbrella of IBM.
- In the present, Ansible comes included in distributions like Fedora Linux, RHEL, Centos and Oracle Linux.

## Important terms used in Ansible

### Ansible Server
- The machine where Ansible is installed and from which all tasks and playbooks will be ran.

### Module
- Basically, a module is a command or set of similar Ansible commands meant to be executed on the client-side.

### Task
- A task is a section that consists of a single procedure to be completed.

### Role
- A way of organising tasks and related files to be later called in a playbook.

### Fact
- Information fetched from the client system from the global variables with the gather-facts operation.

### Inventory
- File containing data about the ansible client servers.

### Play
- Execution of a playbook

### Handler
- Task which is called only if a notifier is present.

### Notifier
- Section attributed to a task which calls a handler if the output is changed.

### Tag
- Name set to a task which can be used later on to issue just that specific task or group of tasks.

## Ansible Installation in Linux

Once you have compared and weighed your options and decided to go for Ansible, the next step is to have it installed on your system. We will go through the steps of installation in different Linux distributions.

### Install Ansible on CentOS/RedHat systems
- Install EPEL Repo
```bash
sudo yum install epel-release
```
- Install ansible package
```bash
sudo yum install ansible
```

### Install Ansible on Ubuntu/Debian systems
- Perform an update to the packages
```bash
sudo apt update
```
- Install the software-properties-common
```bash
sudo apt install software-properties-common
```
- Install ansible personal package archive
```bash
sudo apt-add-repository ppa:ansible/ansible
```
- Install ansible
```bash
sudo apt update
sudo apt install ansible
```

## Ansible ad-hoc commands

One of the simplest ways Ansible can be used is by using ad-hoc commands. These can be used when you want to issue some commands on a server or a bunch of servers. Ad-hoc commands are not stored for future uses but represent a fast way to interact with the desired servers.
```bash
ansible -i hosts all -m ping
```
```bash
host1 | SUCCESS => {
	"changed": false,
	"ping": "pong"
}
host2 | SUCCESS => {
	"changed": false,
	"ping": "pong"
}
```
### Explanation
- "SUCCESS" is the status of the command.
- "host1", "host2" are the host on which the command ran.
- "ping" is the command issued via the -m parameter.
- With the -i parameter, you can point to the hosts file.

```bash
ansible -i hosts all -m ping --limit host2
```
```bash
host2 | SUCCESS => {
	"changed": false,
	"ping": "pong"
}
```
- "--limit" parameter can be used to issue commands only on specific hosts in the host's file.
- "host2", Name of the host as defined in the inventory file.

If you need to copy a file to multiple destinations rapidly, you can use the copy module in ansible which uses SCP. 
```bash
ansible -i hosts all -m copy -a "src=/root/test_ansible/testfile dest=/tmp/testfile"
```
```bash
host1 | SUCCESS => {
	"changed": true,
	"checksum": "da39a3ee......",
	"dest": "/tmp/testfile",
	"gid": 0,
	"group": "root",
	"md5sum": "d41d8c.......",
	"mode": "0644",
	"owner": "root",
	"size": 0,
	"src": "/root/.ansible/tmp/ansible-tmp-156..../source",
	"state": "file",
	"uid": 0
}
host2 | SUCCESS => {
	"changed": true,
	"checksum": "da39a3ee......",
	"dest": "/tmp/testfile",
	"gid": 0,
	"group": "root",
	"md5sum": "d41d8c.......",
	"mode": "0644",
	"owner": "root",
	"size": 0,
	"src": "/root/.ansible/tmp/ansible-tmp-156..../source",
	"state": "file",
	"uid": 0
}
```

### Explanation
- "copy" - Copy module defined.
- "src=...." Module arguments, in this case, are source absolute path and destination absolute path.
- "host1 | SUCCESS => {.....}" - Ansible command output reflecting the success of the copy command and other details like the sha1 and md5 checksums for file integrity check and metadata like owner, size, or permissions.

It is effortless to have a package installed on a bunch of servers. Ansible has several modules that interact with used installers, like yum, apt, dnf, etc.

Now we will learn how to install a package via the yum module on two Centos hosts.
```bash
ansible -i hosts all -m yum -a 'name=ncdu state=present'
```
```bash
host1 | SUCCESS => {
	"changed": true,
	"msg": "",
	"rc": 0,
	"results": [.......]
}
host2 | SUCCESS => {
	"changed": true,
	"msg": "",
	"rc": 0,
	"results": [...........]
}
```
### Explanation
- "yum" - Yum module
- 'name=ncdu state=present' - It defines the module arguments, and in this case, you will choose the name of the package and its state. if the state is absent, the package will be searched and if found, removed.
- "host1 | SUCCESS = > {...}" - When colored in yellow, you will see the output of the ansible command with thw state changed, meaning in this case, that the package was found and installed.
- "results : ......."Status of the yum install command issued via ansible. In this case the package ncdu.x86_64 was installed.

Of course, all of the yum installer options can be used via ansible, including update, install, latest version, or remove.

Now we will learn how to remove the previously installed package.
```bash
ansible -i hosts all -m yum -a 'name=ncdu state=absent'
```

## Ansible Playbooks

Ansible playbooks are the way of sending commands to remote systems through scripts. Ansible playbooks are used to configure complex system environments to increase flexibility by executing a script to one or more systems. Ansible playbooks. tend to be more of a configuration language than a programming language.

Ansible Playbooks commands use YAML format, so there is not much syntax needed, but indentation must be respected. Like the name is saying, a playbook is a collection of plays. Through a playbook, you can designate specific role to some hosts and other roles to other hosts. By doing so, you can orchestrate multiple servers in very diverse scenarios, all in one playbook.

To have all the details precise before continuing with Ansible playbook examples, we must first define a task. These are the interface to ansible modules for roles and playbooks.

Now, let's learn Ansible playbook through an example with one playbook with one play, containing multiple tasks as below:

```bash
---

- hosts: group1
  tasks:
  - name: Install lldpad package
    yum:
      name: lldpad
      state: latest
  - name: check lldpad service status
    service:
       name: lldpad
       state: started
```

