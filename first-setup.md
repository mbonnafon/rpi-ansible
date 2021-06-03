# First setup for headless mode

If you have a fres raspberry pi and want it to be up accessible and configurable with ansible follow theses instructions:

1. Install the desired OS
   Debian 64 bits: https://www.raspberrypi.org/forums/viewtopic.php?t=275370 https://downloads.raspberrypi.org/raspios_arm64/images/

2. Mount the SD card to your OS
   On linux, use `lsblk` to list your devices, select the smallest partition which is the real boot partition. Then mount it to your system with `mount /dev/sdx /mnt/folder`

- Enable SSH by creating a file with the name ssh. It doesn't matter if it's empty or have a content.
  Debian: `touch boot/ssh`
  Ubuntu: `touch /ssh`

- Enable wifi if you can't wire it with an ethernet cable:
  Debian: https://manpages.debian.org/stretch/wpasupplicant/wpa_supplicant.conf.5.en.html
  Ubuntu: https://netplan.io/examples/

- ssh ubuntu@raspberry.local

# Ansible resources:

`ansible all -m ping`
https://docs.ansible.com/ansible/2.8/user_guide/playbooks_best_practices.html

`ansible-playbook role.yml`
https://docs.ansible.com/ansible/latest/user_guide/playbooks_best_practices.html
