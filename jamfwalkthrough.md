Imaging A Mac With JAMF
=====================



Steps to take
--------
* Wipe Computer drive
* Re-install operating System 
* use enroll username and PXE Password on Enroll login
* Log into Tech Support
* Change ComputerName using `sudo scutil --set ComputerName usernameMBP`
* You can check that these changes have been maed using the following commands.

````
sudo scutil --get ComputerName
sudo scutil --get HostName
sudo scutil --get LocalHostName
````
* Once this is done you will make sure to run the recon command to get the computer to check in with Jamf `sudo jamf recon`
* This will trigger jamf to bind the computer to AD and download the manditory settings and applications.



###All Commands used
````
sudo scutil --set ComputerName usernameMBP
sudo scutil --get ComputerName 
sudo scutil --get HostName
sudo scutil --get LocalHostName
sudo jamf recon
````


###Naming Conventions
* MacBook Pro: usernameMBP
* Mac Pro: usernameMP
* iMac: usernameIM
* MacMini: usernameMM
* Loaners: Loaner0000 (Loaner + tag number without the -78)
	


