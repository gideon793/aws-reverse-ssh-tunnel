# aws-reverse-ssh-tunnel
Create a reverse SSH tunnel to AWS.

Useful if you don't have a fixed IP and can't do portforwarding.

Ensure all the usernames and IP addresses are correct and place the aws.service file in /etc/systemd/system to use.

To launch: sudo systemctl start aws.

To launch at boot: sudo systemctl enable aws.

