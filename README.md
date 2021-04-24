# DD-WRT_Utils
Collection of DD WRT Utilities
Most of the consumer routers would delete any pre routing set up after a restart. 
This is done to ensure that any attempt to hack/modify the default route/config via command line is removed once user restarts the node.
Even though it is good from a user experience perspective, it creates problem for forcing hardocded traffic to always go through PiHole.
We can work around it by setting up HardCodedDNSFilter.sh as a job using cron to ensure that pre routing entries are added again after router restart.

create scripts directory
mkdir scripts
cd scripts

Fetch the files from github
wget 
wget

chmod 755 
chmod 755



Add entry to crontab
crontab -e

Then add a new line as shown below:
55 * * * * /home/pi/scripts/HardCodedDNSFilter.sh >>/home/pi/scripts/HardCodedDNSFilter.log 2>&1


