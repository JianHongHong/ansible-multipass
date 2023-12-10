# Creating multiple development servers in macos for testing using multipass

1. To setup new servers:
  - Ensure server names are in `var.yml` this will be referenced in `provison.yml`
  - Ensure mutlipass installed
  - Run `ansible-playbook -i inventory provison.yml`
  - Edit ip address in inventory

2. To remove created servers:
  - Ensure server names are in `var.yml` this will be referenced in `provison.yml`
  - Run `ansible-playbook -i inventory unprovision.yml`

3. Set up inital services in servers:
  - Ensure server names + ip address are in inventory this will be referenced in `provison.yml`
  - Run `ansible-playbook -i inventory setup.yml`