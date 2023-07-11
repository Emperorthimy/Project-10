## **Documentation for Project 10**

### Updating etc Hostfile

![etc-hostfile-update](./Images/etc-hosts.png)

### Configuring Nginx as Load Balancer

`sudo apt update`
`sudo apt install nginx`

![Nginx-Installation](./Images/install-nginx.png)

### Ensuring nginx is up and running

`sudo systemctl restart nginx`
`sudo systemctl status nginx`

![Nginx-status](./Images/nginx-status.png)

## **Configuring Route 53**

### creating hosted zone

![Hosted-Zone-Creation](./Images/route-53.png)

### Name server Configuration

![Nameserver-Config](./Images/domain.png)

### Configuring NginxLB with Webserver Names defined in etc Hostfile

`sudo vi /etc/nginx/nginx.conf`

![nginxLB-config-with-webserver-names-defined-in-ect-hostfiles](./Images/nginx.conf.png)

### Accessing our newly registered Domian from URL

`http://thimy.site/`

![Accessing-our-web-server-using-newly-registered-domain](./Images/success.png)

## Securing our Domain

### Installing Certbot and its dependencies

`sudo apt install certbot -y`
`sudo apt install python3-certbot-nginx -y`

![Installing-certbot-and-its-dependencies](./Images/certbot-install.png)

### Creating a certificate for our Domain to make it secure

`sudo certbot --nginx -d thimy.site -d www.thimy.site`

![creating-certificate-to-secure-our-domain](./Images/test-certbot.png)
