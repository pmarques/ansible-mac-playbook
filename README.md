Mac OS X playbook
=================

A playbook to configure OS X machine with Development and Operations / Administration tools.

# Requirements

First you need to install [homebrew](http://brew.sh/), the playbook will then update when there is an update.

Then you need to install Ansible if you are running the playbook locally, Ansible version needs to be 2.0 or greater.

__NOTE:__ _Check available version, and you can use `--devel` to install latest development version_

```bash
brew install ansible
```

Devel version

```bash
brew install --devel ansible
```

# Provisioning Mac OS X, Configure & Install

```bash
ansible-playbook -i host playbook.yaml --ask-become-pass
```

## Upgrade packages

```bash
ansible-playbook -i hosts playbook.yml -e pkg_state=latest
```
