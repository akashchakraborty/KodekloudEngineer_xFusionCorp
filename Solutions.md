Kodekloud Engineers - Solutions

POSITION: SYSTEM ADMIN

1. TASK 1 - LINUX FILE PERMISSIONS

	Task: 
	There are new requirements to automate a backup process that was performed manually by the xFusionCorp Industries system admins team earlier. 
	To automate this task, the team has developed a new bash script xfusioncorp.sh. They have already copied the script on all required servers, however they did not make it executable on one the app server i.e App Server 1 in Stratos Datacenter.

	Please give executable permissions to /tmp/xfusioncorp.sh script on App Server 1. Also make sure every user can execute it.

	Solution:

		a. Go to the server by ssh and get root access
			```shell
			ssh tony@stapp1
			sudo su -
			```
		b. Now, we go the loaction:
			```shell
			cd /tmp/
			```
		d. There will be a the desired file
			```shell 
			xfusioncorp.sh
			```
		e. We then check the permissions it has
			```shell
			ls -ltr xfusioncorp.sh
			```
		f. As per the task all other users need to have execute permission
			```shell
			chmod o+rx xfusioncorp.sh
			```
		g. Check the changes
			```shell
			ls -ltr xfusioncorp.sh
			sh xfusioncorp.sh
			```
			
