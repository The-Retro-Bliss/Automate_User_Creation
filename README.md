## Automate_User_Creation

# Task

* Your company has employed many new developers. As a SysOps engineer, write a bash script called **create_users.sh** that reads a text file containing the employee’s usernames and group names, where each line is formatted as user;groups. 
* The script should create users and groups as specified, set up home directories with appropriate permissions and ownership, generate random passwords for the users, and log all actions to /var/log/user_management.log. 
* Additionally, store the generated passwords securely in /var/secure/user_passwords.txt. 
* Ensure error handling for scenarios like existing users and provide clear documentation and comments within the script.

# Requirements

* Each User must have a personal group with the same group name as the username, this group name will not be written in the text file. 
* A user can have multiple groups, each group delimited by comma "," 
* Usernames and user groups are separated by semicolon ";"
* Ignore whitespace e.g. \
light; sudo,dev,www-data \
idimma; sudo \
mayowa; dev,www-data \
\
For the first line, light is username and groups are sudo, dev, www-data

# Solution

Create your **create_users.sh** script. You can view the script in the file section. 

To successfully run the create_users.sh script, follow these steps: 

1. Ensure Root User Privileges:
   Before executing the script, make sure you have root user privileges. This is necessary to create users, assign groups, and set permissions.
   
2. The script uses the OpenSSL tool to generate secure, random passwords for new users, so ensure that OpenSSL is installed. 

From here, you can download the create_users.sh script and run it on your machine. Remember to run a text file as an argument. 

e.g bash /opt/scripts/create_users.sh script /opt/scripts/employees.txt

