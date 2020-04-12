# Ansible Role Homebrew

## Install XCode cli tools

```shell script
xcode-select --install
```

## Install Ansible

```shell script
sudo pip install ansible
```

### Create roles directory

```shell script
mkdir -p $USER/Projects/ansible/roles
cd $USER/Projects/ansible
```

### Clone the repository

```shell script
git clone https://github.com/mantoso/mantoso-role-homebrew roles/mantoso-role-homebrew
```

### Create Playbook

```shell script
cp roles/mantoso-role-homebrew/homebrew-playbook-example.yml homebrew-playbook.yml
```

Or if you are ok with the example playbook, create a symlink to it:

```shell script
ln -s $(pwd)/roles/mantoso-role-homebrew/homebrew-playbook-example.yml $(pwd)/homebrew-playbook.yml
```

### Run ansible-playbook

```shell script
ansible-playbook --ask-become-pass homebrew-playbook.yml
```
