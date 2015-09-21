# Nginx_on_Redhat-7
### installation

 Create a file to discover the repository URL 
* `sudo vi /etc/yum.repos.d/nginx.repo`

 past following contents in the file
 ```
 [nginx]
 name=nginx repo
 baseurl=http://nginx.org/packages/rhel/7/$basearch/
 gpgcheck=0
 enabled=1
 ```
 install the nginx
* `sudo yum install nginx.x86_64`

 start service
* `sudo service nginx start`

### Virtual Host on redhat7-nginx

 create root Directory
 
* `mkdir /usr/share/nginx/html/nginadnan`
* copy the default configration file or make new

* `cp /etc/nginx/conf.d/default.conf /etc/nginx/conf.d/adnan.conf`
* edit the new file `adnan.conf`

* `vi /etc/nginx/conf.d/adnan.conf`
* change the server name and root directory

* make index.html page in nginadnan
* `/usr/share/nginx/html/nginadnan/index.html`

* open the host file and enter IP address and server name in it
* `vi /etc/hosts/`
* restart the nginx server
* ` systemctl restart nginx.service`
* open your browser and type nginx.adnan.com

