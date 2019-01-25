# HiveConfiguration
Storing of Hadoop and Hive Configuration

Create a Google Cloud Instance with n1-standard-2 (2 vCPUs, 7.5 GB memory) configuration. I have choosen Ubuntu 16.04 with Standard Persistent disk size of 100GB.

#### Setting Up SSH and root Configuration

Once the instance is started, add sudo permissions to it and provide password command. It will ask to create new password.

1. sudo -i
2. passwd

Create new Password:

Next step is to configure SSH to access through putty from your local machine. open the below file and make below changes
vi /etc/ssh/sshd_config

1. PermitRootLogin yes
2. AuthorizedKeysFile      /root/.ssh/authorized_keys
3. ChallengeResponseAuthentication yes
4. PasswordAuthentication yes

Save the file changes using **:wq!** command from your vi editor and restart the ssh 

ssh service restart

Now copy the External IP from your VM Instance page and try connecting using putty. If you able to connect succesfully then you are good to go. If it is failed to connect, then check VPC Firewall rules in cloud and make sure to change default-allow-internal ip range to **0.0.0.0/0**



