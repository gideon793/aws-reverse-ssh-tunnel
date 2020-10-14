# aws-reverse-ssh-tunnel
Create a reverse SSH tunnel to AWS.

Useful if you don't have a fixed IP and can't do portforwarding.

Ensure all the usernames and IP addresses are correct and place the aws.service file in /etc/systemd/system to use.

To launch: sudo systemctl start aws.

To launch at boot: sudo systemctl enable aws.

Create a file at /etc/nginx/sites-enabled/*public URL*

Add the following contents:
server {
    server_name *public URL*;
    listen 80;
    location / {
    proxy_pass  http://127.0.0.1:10002;
}
}

Check nginx -t and restart service
