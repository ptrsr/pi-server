# PI-SERVER
A preconfigured pi-hole, built using [PI-TEMPLATE](https://github.com/ptrsr/pi-template). Includes;

- Auto start on power on.
- Customizable using a single, simple config.
- Extendable using Ansible.
- Configure containers using docker-compose.
- Set up the server using a single command.

Download the latest release on the [releases page](https://github.com/ptrsr/pi-server/releases).

This repository uses Github Actions to prepare Raspberry Pi images, enabling [configurations to be defined as code](https://www.redhat.com/en/topics/automation/what-is-infrastructure-as-code-iac) through Ansible.
Every commit represents a snapshot of a RPi configuration, which can be reproduced by flashing the image on an SD card and running the provided Ansible playbooks.

## Usage
1. Flash the [latest release](https://github.com/ptrsr/pi-server/releases) to an SD card.
2. Log or SSH into the RPi using `root` (no password required).
3. Change the configuration (like the username and password) in the `/root/template/inv/local.yml` file.
4. Run `/root/template/run.sh local` to apply the configuration and start the containers!

The docker containers will automatically start when the RPi is rebooted.

## License
PI-SERVER is licensed under [GPLv3](https://www.gnu.org/licenses/gpl-3.0.en.html).
