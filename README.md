# devops-cmds
Covers most commonly used list of commands in daily devops. Feel free to add if anything missing.

# AWS EC2

Update Aws .pem file permisson for ssh to EC2
`chmod 400 aws-keypair.pem`

SSH to aws ec2
`ssh -i aws-keypair.pem ec2-user@hostaddress`

# Docker

Docker installation on aws ec2 linux

`sudo yum update -y`

For Amazon Linux 2023, run the following:

`sudo yum install -y docker`

Start the Docker service.

`sudo service docker start`

Add the ec2-user to the docker group so that you can run Docker commands without using sudo.

`sudo usermod -a -G docker ec2-user`

Pick up the new docker group permissions by logging out and logging back in again. To do this, close your current SSH terminal window and reconnect to your instance in a new one. Your new SSH session should have the appropriate docker group permissions.

Verify that the ec2-user can run Docker commands without using sudo.
`docker ps`
