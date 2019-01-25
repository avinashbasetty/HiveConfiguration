# HiveConfiguration
Storing of Hadoop and Hive Configuration

Create a Google Cloud Instance with n1-standard-2 (2 vCPUs, 7.5 GB memory) configuration. I have choosen Ubuntu 16.04 with Standard Persistent disk size of 100GB.

#### Setting Up SSH and root Configuration

Once the instance is started, add sudo permissions to it and provide password. It will ask to create new password.

sudo -i
passwd
Create new Password:

Next step is to configure SSH to access through putty from your local machine. open the below file and make below changes
vi /etc/ssh/sshd_config

PermitRootLogin yes
AuthorizedKeysFile      /root/.ssh/authorized_keys
ChallengeResponseAuthentication yes
PasswordAuthentication yes

Save the file changes using **:wq!** command from your vi editor and restart the ssh using **ssh service restart** command

Now copy the External IP from your VM Instance page and try connecting using putty.
