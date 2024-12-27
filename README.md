# Documentation on setting up the server, installed the web server, deployed the HTML page, and configured networking

-> Public IP address - http://18.184.216.143/

# How I Installed Ubuntu through cloud platform (AWS)
-> I signed in to my AWS console account
-> Clicked on EC2
-> I chose Frankfurt as my location
-> Navigated to Lauch the Instance
-> Assigned a name to the Instance
-> Selected Ubuntu as the operating system to be used
-> Selected 64-bit(84) as the architecture
-> Selected t2-micro as the Instance type
-> Created a key-pair
-> Set-up the firewall as Allow SSH traffic from Anywhere, Allow HTTPS traffic from the internet and Allow HTTP traffic from the internet
-> I gave the storage configuration for the machine as 30gb
-> I clicked on Lauch Instance to lauch the machine I just created

# How to set up the Apache
-> sudo apt update
-> sudo apt install apache2
# To check if the apache is running
-> sudo systemctl status apache2
# To get local IP address
-> ip addr show
# For public IP (if the server is exposed to the internet)
-> curl ifconfig.me
# Test Apache Installation: Open a web browser and navigate to your server's IP address or localhost
-> http://your-server-ip
# To Start Apache
-> sudo systemctl start apache2
# To Stop Apache
-> sudo systemctl stop apache2
# To Restart Apache
-> sudo systemctl restart apache2
# To Enable Apache to Start on Boot
-> sudo systemctl enable apache2
# To Disable Apache from Starting on Boot
-> sudo systemctl disable apache2

# Check Ownership and Permissions on the var/www/html

# To check the current permissions
-> ls -ld /var/www/html
# Change Ownership
-> sudo chown -R $USER:$USER /var/www/html
# Change Permissions
-> sudo chmod -R 755 /var/www/html


# HTML and CSS Page
-> Create a simple HTML page with an inline CSS on VS Code
-> copied and pasted the code on file index.html on var/www/html

# To deploy html page on vercel
-> Create a Vercel Account (www.vercel.com)
-> 
