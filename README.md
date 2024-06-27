# aws_demo
Deploying a static Website to AWS EC2 with NGINX

Prerequisites:

AWS Account:
* Ensure you have an AWS account. If not, sign up for one.
* EC2 Instance:

* Launch an EC2 instance with Ubuntu 22.04. Make a note of the instance's public IP or DNS.
* Security Group:
* Configure the security group to allow traffic on ports 80 (HTTP) and 22 (SSH).
* SSH Key Pair:
* Create or use an existing SSH key pair to connect to the EC2 instance.


Steps:
1. Connect to your Ubuntu EC2 instance:

ssh -i /path/to/your/key.pem ubuntu@your-instance-ip

2. Update the system:

sudo apt update && sudo apt upgrade -y

3. Install NGINX:

sudo apt install nginx -y

4. Start NGINX:

sudo systemctl start nginx

5. Clone your GitHub repository:

#First navigate to /var/www/html
cd /var/www/html

# Then initialize git
git init

#Clone git repo
git clone https://github.com/your-username/your-repo.git

6. Configure permissions:

sudo chown -R www-data:www-data /var/www/html

7. Verify NGINX configuration:

sudo nginx -t

8. Reload NGINX:

sudo systemctl reload nginx

9. Set up a domain (optional):
If you have a domain, configure your DNS settings to point to the EC2 instance's public IP.

10. Access your website:
Open a web browser and navigate to your EC2 instance's public IP. Your simple HTML/CSS website is now live and accessibl.

