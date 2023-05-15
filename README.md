# PI-SERVER
A preconfigured pi-hole, built using [PI-TEMPLATE](https://github.com/ptrsr/pi-template). Set up a complete pi-hole server on a Raspberry Pi with a single command! Includes;

- Auto start on power on.
- Customizable through Ansible.
- Personalizable with inventory files.
- Simply add or configure servers using `data/server/docker-compose.yml`.
- Easy to use, just run `./run.sh local`.

Download the latest release on the [releases page](https://github.com/ptrsr/pi-server/releases).

This repository uses Github Actions to prepare Raspberry Pi images, enabling [configurations to be defined as code](https://www.redhat.com/en/topics/automation/what-is-infrastructure-as-code-iac) through Ansible.
Every commit represents a snapshot of a RPi configuration, which can be reproduced by flashing the image on an SD card and running the included Ansible playbooks (provided in this repo).

## Usage
1. Flash the [latest release](https://github.com/ptrsr/pi-server/releases) to an SD card.
2. Log or SSH into the RPi using `root` (no password required).
3. Change the configuration (like the username and password) in the `local.yml` file.
4. Run `./run.sh local` to apply the configuration and start the containers!

The docker containers will automatically start on boot.

## License
PI-SERVER is licensed under [GPLv3](https://www.gnu.org/licenses/gpl-3.0.en.html).
