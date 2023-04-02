# Find-Command
KodeKloud - SystemAdministrator
##### During a routine security audit, the team identified an issue on the Nautilus App Server. Some malicious content was identified within the website code. After digging into the issue they found that there might be more infected files. Before doing a cleanup they would like to find all similar files and copy them to a safe location for further investigation. Accomplish the task as per the following requirements:

##### a. On App Server 1 at location /var/www/html/beta find out all files (not directories) having .php extension.

##### b. Copy all those files along with their parent directory structure to location /beta on same server.

##### c. Please make sure not to copy the entire /var/www/html/beta directory content.

###### Login to appserver and switch root user.
```
ssh tony@stapp01
sudo su -
```
##### Locate the directory and find the files with .php extension and copy to /beta

```
cd /var/www/html/
ls
find /var/www/html/beta -name '*.php' -exec cp --parents {} /beta \;
````

#### Happy learning!




