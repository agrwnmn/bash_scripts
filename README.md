# bash_scripts

These scripts are helpful tools that allows for repeatable tasks. 

KNOWN-HOST-KEY_Removal bash script:
  This script automatically removes the ssh key in your known_host file. Often times RSA Key fingerprints will change and will not allow you to SSH into your         intended host. This script allows you to view the known_host file to confirm there is an entry in the known_host file for this host. It also allows you to remove   the old/existing RSA host-key from the known_hosts file

To view if a host key is in the known_host folder
  bash known_host_key_removal.sh -h z-cleep-asw-201 -p
  
  Possible entries to search for:
 * z-cleep-asw-201

Entries located in /home/lacarter/.ssh/known_hosts file
 * z-cleep-asw-201
Usage:
  known_host_key_removal.sh -h hostname -p 22 -H -k ~/.ssh/known_hosts [-a|-r|-p]

Parameters:
  -h hostname    : set SSH hostname (required)
  -k known_hosts : set SSH known hosts file location (default is "~/.ssh/known_hosts")
  -P port        : set SSH port (default is  "22")

Actions:
  -r             : remove host entries for the provided hostname
  -p             : print host entries related to the provided hostname


To remove a host key from the known_host folder
  bash known_host_key_removal.sh -h z-cleep-asw-201 -p
  
  Entries removed: 1
Usage:
  known_host_key_removal.sh -h hostname -p 22 -H -k ~/.ssh/known_hosts [-a|-r|-p]

Parameters:
  -h hostname    : set SSH hostname (required)
  -k known_hosts : set SSH known hosts file location (default is "~/.ssh/known_hosts")
  -P port        : set SSH port (default is  "22")

Actions:
  -r             : remove host entries for the provided hostname
  -p             : print host entries related to the provided hostname

