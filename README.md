# CNTRL

This is a simple repository used to collect scipts and configurations usefull for some projects in **Casa Jasmina**.

# Ansible

Here there are a set of ansible's script for deploy a local server on a **Raspberry Pi 2**.
Above the list of contents.

### Content
* [Ansible](http://www.ansible.com/)
  * [Mosquitto](http://mosquitto.org/)
  * [Emqtt](https://github.com/emqtt)
  * Debian (basic conf)
  * [Xbmc](http://kodi.tv/)

### TODO

- [ ] Add daemon configurations
- [x] Basic xbmc integration
- [x] Inlcude mosquitto/xbmc conf


### Setting the script up

* Install Ansible in your local machine -> [follow the guide for your os](https://docs.ansible.com/ansible/intro_installation.html)
* Git clone this repository
```
$ git clone git@github.com:CasaJasmina/CNTRL.git
$ cd CNTRL
$ git checkout master
```
* Edit vars configurations files `ansible/global_vars/main.yml`
* Set your hosts `ansible/hosts`

### Deploy a complete installation

**Warning:** before you running the script you must ensure that you have properly configure the ssh-key for all your hosts
```
$ ansible-playbook -i ansible/hosts ansible/site.yml
```
If you can't establish a secure connection with an ssh-key you can prompt a password for the remote user with:
```
$ ansible-playbook -i ansible/hosts -k -K ansible/site.yml
```
#### Deploy on Localhost
If you want to correctly run the script in localhost add this line to the `/etc/ansible/hosts` file
```
# Localhost connection
localhost ansible_connection=local
```
and set `lolcahost` in the `ansible/hosts` configuration file

### Atomic installation
**TODO**


### Running on Vagrant
**TODO**
