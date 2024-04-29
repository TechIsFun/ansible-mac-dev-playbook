# Mac Development Ansible Playbook

![ci](https://github.com/TechIsFun/ansible-mac-dev-playbook/actions/workflows/ci.yml/badge.svg)

Inspired by https://github.com/geerlingguy/mac-dev-playbook

This playbook installs and configures most of the software I use on my Mac for web and software development. Some things in macOS are slightly difficult to automate, so I still have a few manual installation steps, but at least it's all documented here.

## Installation

  1. Ensure Apple's command line tools are installed (`xcode-select --install` to launch the installer).
  2. Install Ansible using `brew install ansible` or by following [Ansible Install Guide](https://docs.ansible.com/ansible/latest/installation_guide/index.html):

  3. Clone or download this repository to your local drive.
  4. Run `ansible-galaxy install -r requirements.yml`
  5. Run `ansible-playbook main.yml --ask-become-pass` inside this directory. Enter your macOS account password when prompted for the 'BECOME' password.

> Note: If some Homebrew commands fail, you might need to agree to Xcode's license or fix some other Brew issue. Run `brew doctor` to see if this is the case.

## Package specific setup

### Espanso

Run `espanso register` to enable accessibility
