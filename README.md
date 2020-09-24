# Bash-Script-For-Automation
A bash script and systemd service file for automating in startup
A simple systemd service file which will run a bash script command to  set the speaker volume to a hundred since the solus 4.1 os alsamixer does not have support for older sound card 
Place the bash script in the location /etc/init.d/
Similarly place the service file in /etc/systemd/system/

give the relevant permissions for the sevice file with the command
$ sudo chmod 644 /etc/systemd/system/alsamixer.service

Now enable the service for it to start at bootup
$ sudo systemctl enable alsamixer.service

To start the service use the command
$ sudo systemctl start alsamixer.service

To stop the service use the command
$ sudo systemctl stop alsamixer.service
