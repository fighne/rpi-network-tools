# rpi-tcpdumpd

Installing tcpdumpd along with systemd configs to run the process

Install PolicyKit 1 "sudo apt-get install policykit1"

copy the file tcpdumpd.service in this repository into the following directory /etc/systemd/services

Within the file are the settings which tcpdump will use in the example one it's setup to rotate the files

run "sudo systemctl daemon-reload" this reloads systemd daemons list

run "sudo systemctl start tcpdumpd" this starts the daemon/service

run "sudo systemctl enable tcpdumpd" this enables the service to start of bootup automatically
