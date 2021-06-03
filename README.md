# rpi-ansible

This will set up a new Raspberry with Ubuntu in order to use k3s.

# usage

Provide your wifi SSID and password as extra vars.

Command: `ansible-playbook role.yml --extra-vars "{\"wifi_ssid\":\"MySSID\", \"wifi_psk\":\"MyPasswd\"}"`

# notes

Temporary use k3s role and install it manually. Target is to use: https://github.com/k3s-io/k3s-ansible
