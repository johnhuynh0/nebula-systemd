# Installation
1. Clone a copy of this repository.
   ```bash
   $ git clone https://github.com/johnhuynh0/nebula-systemd.git`
   ```
2. Copy it into the global directory for systemd unit files.
   ```
   $ cd nebula-systemd
   $ sudo cp nebula.service /etc/systemd/system/
   ```

3. Copy your [config.yml](https://nebula.defined.net/docs/) file to `/etc/nebula/`.

# Usage
- Enable the service to start on boot: `sudo systemctl enable nebula`
- Disable the service from starting on boot: `sudo systemctl disable nebula`
- Start the service: `sudo systemctl start nebula`
- Stop the service: `sudo systemctl stop nebula`

# Monitoring
- `journalctl --follow --unit nebula` (can be shortened to `journalctl -fu nebula`)

# Tips and tricks
- Enable and start the service at the same time: `sudo systemctl enable --now nebula`
- Disable and stop the service at the same time: `sudo systemctl disable --now nebula`
